---
title: "Gitignore: Ignoring files in your Git repository"
seoTitle: "Gitignore: Ignoring files in your Git repository"
seoDescription: "There may be files or directories in your project that you don't want to track or include in your Git repository. This is where Gitignore comes in"
datePublished: Sun Apr 09 2023 05:48:38 GMT+0000 (Coordinated Universal Time)
cuid: clg8zhzwe05ekpxnv8rmgg677
slug: gitignore-ignoring-files-in-your-git-repository
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1680855368785/e312277b-3f82-4649-bae7-27e48e4e4067.jpeg
tags: github, version-control, git, 2articles1week, gitignore

---

Git is a powerful version control system that helps developers keep track of changes made to their codebase. However, there may be files or directories in your project that you don't want to track or include in your Git repository. 

This is where Gitignore comes in. Gitignore is a feature that allows you to specify files or directories that Git should ignore when you commit changes to your repository. 

## Step 1: Create a Git repository

The first step in using Gitignore is to create a Git repository. You can create a new repository from scratch or clone an existing one from a remote server. To create a new repository, navigate to the directory where you want to store your project and run the following command:

```bash
git init
```

This will initialize a new Git repository in your current directory.

## Step 2: Create a .gitignore file

The next step is to create a .gitignore file. This file is a simple text file that contains a list of files or directories that Git should ignore. To create a .gitignore file, run the following command in your terminal:

```bash
touch .gitignore
```

This will create a new file called ".gitignore" in your current directory.

## Step 3: Add files or directories to .gitignore

Now that you have created a `gitignore` file, you can start adding files or directories to it that you want Git to ignore. 

To do this, simply open the `.gitignore` file in a text editor and add the names of the files or directories that you want to exclude from your repository.

For example, if you want to exclude all files with the .log extension, you can add the following line to your `.gitignore` file:

```bash
*.log
```

This will tell Git to ignore all files with the .log extension in your repository.

Other files that can be excluded are the  `"node_modules"` directory, which contains all of the dependencies for a Node.js project. To exclude the `"node_modules"` directory from your Git repository, simply add the following line to your `.gitignore` file:

```bash
node_modules/
```

This will tell Git to ignore the entire "node\_modules" directory in your repository. You can also use wildcard characters to ignore all directories with a specific name, like this:

```bash
**/node_modules/
```

This will ignore all directories named "node\_modules" in your repository, regardless of their location.

## Step 4: Commit changes to the Git repository

Once you have added the files or directories that you want to ignore to your Gitignore file, you can commit your changes to your Git repository. To do this, run the following commands in your terminal:

```bash
git add .
git commit -m "Added .gitignore file
```

This will add your Gitignore file to your repository and commit your changes with a message that says "Added .gitignore file".

## Step 5: Verify Gitignore is working

To verify that .`gitignore` is working, create a new file with the extension that you added to your .`gitignore` file. For example, if you added `*.log` to your Gitignore file, and create a new file called "test.log" in your repository. Then, run the following command:

```bash
git status
```

This will show you the status of your Git repository. You should see that the file "test.log" is not being tracked by Git.  

*Note that when you add a file or directory to the gitignore file, Git will not track any changes made to that file or directory.*

If you want to track changes to a file or directory that you have previously ignored, you will need to remove it from the .`gitignore` file and then add it to your Git repository using the `"git add"` command.

Using Gitignore is an essential part of managing your Git repository. When you exclude files or directories that you don't want to track, you can keep your repository clean and organized.

This guide has provided you with a step-by-step tutorial on how to use Gitignore via the command line to exclude files or directories from your Git repository.  
  
Happy Git-ing!