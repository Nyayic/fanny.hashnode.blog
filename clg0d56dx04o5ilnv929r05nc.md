---
title: "Introduction to WordPress and Setting up Development Environment Using XAMPP"
seoTitle: "Introduction to WordPress and setting up Development Environment"
seoDescription: "WordPress is a free and open-source content management system. It allows you to create and manage websites, blogs, and online stores."
datePublished: Mon Apr 03 2023 05:00:39 GMT+0000 (Coordinated Universal Time)
cuid: clg0d56dx04o5ilnv929r05nc
slug: introduction-to-wordpress-and-setting-up-development-environment-using-xampp
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1708760970431/d256a763-982c-427c-8ecd-9f15a340a829.png
tags: web-development, xampp, 2articles1week

---

WordPress is a versatile platform that can be used to build anything from simple blogs to complex e-commerce websites. Grab a cup of coffee, put on your thinking cap, and let's dive into the basics of WordPress and setting up development environment with xampp.

## First, What is WordPress?

This is a free and open-source content management system (CMS) that powers over 40% of all websites on the internet. Wordpress provides a user-friendly interface for creating, editing, and publishing content, making it an ideal choice for beginners and experts alike.

One of the most significant advantages of WordPress is its flexibility. With thousands of themes and plugins available, you can customize your website to meet your specific needs.

WordPress is also built using PHP programming language and MySQL as a database server, which is widely used, making it easy to find support and resources online.

## Setting up your development environment

Before we dive into creating a WordPress website, we need to set up what we call a development environment. A **development environment** is a place where you can build and test your website locally before publishing it to the internet.

XAMPP is a popular software bundle that includes everything you need to run a local web server on your computer.

### Step 1: Install XAMPP

The first step is to download XAMPP from the [Apache Friends](https://www.apachefriends.org/). Choose the version that is compatible with your operating system.  

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679729043731/ecdba882-7de0-452e-9a32-4cbef594305f.png align="center")

Download it then run the `.exe` file to start the installation process.

During the installation, you will be asked to select the components you want to install. For our purposes, we need to ensure that Apache, MySQL, and PHP are selected.

### Step 2: Start XAMPP and Test the Server

Once XAMPP is installed, start the software by clicking on the XAMPP Control Panel shortcut on your desktop. 

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679729117321/ec44e073-37e8-477b-b7a1-ed4e003537aa.png align="center")

Click the `Start` buttons next to Apache and MySQL to start the server. If the server is running correctly, you should see a green indication next to each of these components.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679729176445/e560ff6d-92d6-4816-abc3-a0ea2b9bc3a4.png align="center")

To test that the server is working correctly, open your web browser and type "[localhost](http://localhost)" in the address bar.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679729235244/8210e6e4-fee2-4097-ad2a-d1334a4341bf.png align="center")

If everything is set up correctly, you should see the XAMPP welcome page as shown above.

## Step 3: Download WordPress

Now that our development environment is set up, we can download and install WordPress. Head over to [WordPress](https://wordpress.org/download/) website and download the latest version of WordPress. 

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679729282649/946c0b42-aee4-4e52-bce6-4904324ab35c.png align="center")

Extract the files from the downloaded ZIP file.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679729335285/17f05656-9c54-458b-ac53-78814e3ec612.png align="center")

After extracting, copy the entire WordPress folder.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679729386629/cdfb62e8-8912-421d-aba1-cf9e0b536715.png align="center")

And paste it into the **"htdocs"** folder of your XAMPP installation directory ie: `C:\xampp\htdocs`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679729424353/7aa91422-0106-4c1f-a283-75703dc496d6.png align="center")

### Step 4: Create a Database for WordPress

Before we can install WordPress, we need to create a database to store our website's content. To do this, open your web browser and go to "[localhost/phpmyadmin](http://localhost/phpmyadmin)" 

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679729464570/86dc2120-cf37-4161-bf00-8a0f62bbae7d.png align="center")

This will take you to the phpMyAdmin interface, where you can manage your MySQL databases.

Click on the **"Databases"** tab, Then Click **"New"**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679730188543/93413a8f-be52-455b-84a0-6316c21d7c1b.png align="center")

Enter the name for your database, in our example, it is **"wptest"** and click **"Create."**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679730310516/307e62a6-320a-4779-a28b-66927b3a459f.png align="center")

You will be able to see your newly created database in your list of Databases.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679730348735/5df0ea92-1d01-4372-8c9e-66fc67cfb418.png align="center")

### Step 5: Install WordPress

With our database created, we can now install WordPress. Open your web browser and navigate to "[localhost/wordpress](http://localhost/wordpress)." 

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679730425405/fcbb1d5f-2e8b-425a-904f-7d63149a4ee6.png align="center")

Click **"Let's Go"** at the bottom to start the installation process.

You will be asked to enter your database name in our case it is `wptest`, username which is the default `“root”`, a password that we do not have and shall leave empty, and host”, which should be "[`localhost`](http://localhost)`.`" Table prefix, which you can change to your preferred if you want to.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679730556769/220227d1-cb1c-4d7b-8898-8fbcac4ae2f2.png align="center")

Once you have entered the required information, click **"Submit."**

After a successful connection to the database, You can now start running the Installation by clicking on **"Run Installation"**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679731047003/e3777831-ac73-414a-ac4a-9c65eed10cc8.png align="center")

You will be prompted to **add a site title,** **create a username** and **password** for your WordPress site. Then Click **"Install Wordpress"**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679730730186/df0460a9-82dd-400e-9269-bacd943cd335.png align="center")

Congratulations, you've now set up your development environment using XAMPP and installed WordPress.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679731496821/a54719bf-cf11-4ab4-9d20-b63cc4f4da2e.png align="center")

Now you can login using the **username** and **password** you created.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679731612482/58b15892-30df-4fa7-88f0-db53ffb19c33.png align="center")

And Tada!! you are redirected to your WordPress Dashboard.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679731679233/9977cb7b-cd15-4c7c-a140-c144d3b34847.png align="center")

From here, you can start doing the magic of your website creation process, installing themes and plugins, and publishing content.

If you have any questions, feel free to drop a comment!

Happy Installation!