---
title: "How to Build a Note-taking App using PHP"
datePublished: Thu Apr 27 2023 15:58:20 GMT+0000 (Coordinated Universal Time)
cuid: clh7vwo9o000a09mra7w1co4g
slug: how-to-build-a-note-taking-app-using-php
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1683128970516/ebbefa00-24be-46ac-8770-d3550dcda384.jpeg
tags: php, 2articles1week, codenewbies

---

What we are building and how it works:

* User creates a note and is stored in the database.
    
* user views the notes created and displayed.
    
* user can edit the notes created
    
* user can delete the notes from the database
    

## Step 1: Set Up Your Development Environment

Before you begin coding, you'll need to set up your development environment. You can use a local development environment like XAMPP or WAMP.

Assuming you're using XAMPP, download and install it from [https://www.apachefriends.org/index.html](https://www.apachefriends.org/index.html). Once installed, start the Apache and MySQL modules as shown below!  

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683129430347/79dc8ff2-0cfd-4bfa-b6dc-ef94a402f574.png align="center")

## Step 2: Create a Database

The first step in creating a note-taking app is to create a database to store your notes. You can use MySQL, PostgreSQL or any other database that supports PHP. Create a table to store your notes with columns like id, title, content, and timestamp.

Create a database in phpMyAdmin by navigating to [http://localhost/phpmyadmin/](http://localhost/phpmyadmin/) and clicking on the "New" button.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683129213640/a80cbfbc-e2ac-4b77-b1ec-cb70d98abb49.png align="center")

Name the database `"notes_db"` and create a table called `"notes"` with the following columns:

```sql
id (int, primary key, auto_increment)
title (varchar(255))
content (text)
timestamp (datetime)
```

## Step 3: Create a Web Page for Users to Create Notes

Create a webpage where users can create notes. This webpage should have a form with fields for title and content. When the user submits the form, the data should be saved in the database.

```php
<?php
// Connect to the database
$host = "localhost";
$user = "root";
$password = "";
$dbname = "notes_db";
$conn = mysqli_connect($host, $user, $password, $dbname);
// Handle form submission
if ($_SERVER["REQUEST_METHOD"] == "POST") {
  // Get form data
  $title = $_POST["title"];
  $content = $_POST["content"];
  // Insert data into the database
  $sql = "INSERT INTO notes (title, content) VALUES ('$title', '$content')";
  mysqli_query($conn, $sql);
  // Redirect to the display page
  header("Location: index.php");
  exit();
}
?>
<html>
<head>
  <title>Create a Note</title>
</head>
<body>
  <h1>Create a Note</h1>
  <form method="post" action="<?php echo htmlspecialchars($_SERVER["PHP_SELF"]);?>">
    <label for="title">Title:</label><br>
    <input type="text" name="title"><br>
    <label for="content">Content:</label><br>
    <textarea name="content"></textarea><br>
    <input type="submit" value="Create">
  </form>
</body>
</html>
```

## Step 4: Create a Webpage to Display Notes

Create a webpage to display all the notes stored in the database. Use PHP to query the database and retrieve the notes. Display the notes on the webpage in a user-friendly way.

```php
<?php
// Connect to the database
$host = "localhost";
$user = "root";
$password = "";
$dbname = "notes_db";
$conn = mysqli_connect($host, $user, $password, $dbname);
// Retrieve notes from the database
$sql = "SELECT * FROM notes";
$result = mysqli_query($conn, $sql);
?>
<html>
<head>
  <title>My Notes</title>
</head>
<body>
  <h1>My Notes</h1>
  <a href="create.php">Create a Note</a>
  <table>
    <thead>
      <tr>
        <th>Title</th>
        <th>Content</th>
        <th>Date</th>
        <th></th>
      </tr>
    </thead>
    <tbody>
      <?php while ($row = mysqli_fetch_assoc($result)) { ?>
        <tr>
          <td><?php echo $row["title"]; ?></td>
          <td><?php echo $row["content"]; ?></td>
          <td><?php echo $row["timestamp"]; ?></td>
          <td>
            <a href="edit.php?id=<?php echo $row["id"]; ?>">Edit</a>
            <a href="delete.php?id=<?php echo $row["id"]; ?>">Delete</
            </td>
        </tr>
      <?php } ?>
    </tbody>
  </table>
</body>
</html>
```

## Step 5: Add Functionality to Edit notes

Create a new file called "edit.php" in the htdocs directory of your XAMPP installation. Add the following code:

```php
<?php
// Connect to the database
$host = "localhost";
$user = "root";
$password = "";
$dbname = "notes_db";
$conn = mysqli_connect($host, $user, $password, $dbname);
// Handle form submission
if ($_SERVER["REQUEST_METHOD"] == "POST") {
  // Get form data
  $id = $_POST["id"];
  $title = $_POST["title"];
  $content = $_POST["content"];
  // Update data in the database
  $sql = "UPDATE notes SET title='$title', content='$content' WHERE id=$id";
  mysqli_query($conn, $sql);
  // Redirect to the display page
  header("Location: index.php");
  exit();
}
// Retrieve note from the database
$id = $_GET["id"];
$sql = "SELECT * FROM notes WHERE id=$id";
$result = mysqli_query($conn, $sql);
$row = mysqli_fetch_assoc($result);
?>
<html>
<head>
  <title>Edit Note</title>
</head>
<body>
  <h1>Edit Note</h1>
  <form method="post" action="<?php echo htmlspecialchars($_SERVER["PHP_SELF"]);?>">
    <input type="hidden" name="id" value="<?php echo $row["id"]; ?>">
    <label for="title">Title:</label><br>
    <input type="text" name="title" value="<?php echo $row["title"]; ?>"><br>
    <label for="content">Content:</label><br>
    <textarea name="content"><?php echo $row["content"]; ?></textarea><br>
    <input type="submit" value="Save">
  </form>
</body>
</html>
```

## Step 6: Functionality to Delete notes

Create a Webpage to Delete Notes

Create a new file called `"delete.php"` in the htdocs directory of your XAMPP installation. Add the following code:

```php
<?php
// Connect to the database
$host = "localhost";
$user = "root";
$password = "";
$dbname = "notes_db";
$conn = mysqli_connect($host, $user, $password, $dbname);

// Delete note from the database
$id = $_GET["id"];
$sql = "DELETE FROM notes WHERE id=$id";
mysqli_query($conn, $sql);
// Redirect to the display page
header("Location: index.php");
exit();
?>
```

## Note:

You can create a file called `db.php` and add the database connection to it instead of having it in a new file.

```php
<?php 
// connect to database
$conn = new mysqli("localhost","root","","notes_db");
// check connection
if($conn->connect_error){
    die("Connection Failed" .$conn->connect_error);
}
?>
```

Then refer to each file as shown below.

```php
<?php
include('db.php');
?>
```

You can style your user interface and fully customize it. Here is the [Github repository](https://github.com/Nyayic/note-taking-app) to this project.