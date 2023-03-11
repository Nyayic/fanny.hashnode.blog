---
title: "Git basics: Understanding Commits, Branches, and Merges"
seoTitle: "Git basics: Understanding Commits, Branches, and Merges"
seoDescription: "Without a version control system like Git, it would be challenging to keep track of who made what changes and when."
datePublished: Sat Mar 11 2023 05:00:39 GMT+0000 (Coordinated Universal Time)
cuid: clf3i0kgu00ugdlnv5iyhbqwf
slug: git-basics-understanding-commits-branches-and-merges
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1678283127747/1c922e96-3afc-4bd8-a207-417811d30067.png
tags: version-control, git

---

Are you new to Git and feeling overwhelmed by all the technical jargon? Don't worry, you're not alone! Git can be a bit challenging at first, but once you understand the basics, it's an incredibly powerful tool for managing code and collaborating with others on a project.

In this post, let's cover the fundamental concepts of Git: understanding commits, branches, and merges. Let us together break down these concepts into easy-to-understand explanations and real-life examples that will help you grasp the concepts quickly and easily.

Whether you're a complete beginner to Git or you've dabbled in it before and want to refresh your knowledge, this blog post is for you. So grab a cup of coffee, get comfortable, and let's dive into the world of Git together!

## What is Git?

**Git** is a distributed version control system that allows developers to track changes to their source code over time. With Git, you can save snapshots of your code at different stages of development, collaborate with others, and easily roll back to previous versions if needed.

Imagine you are working on a team project with your colleagues. Each of you has a copy of the project files on your local computer, and you are making changes to these files to add new features or fix bugs.

Without a version control system like Git, it would be challenging to keep track of who made what changes and when. You might end up with multiple versions of the same file, with no easy way to merge them into one coherent version.

This is where Git comes in. When you use Git to manage your project, you create a repository that acts as a central hub for all the project files.

Each time you make changes to a file, you create a commit that records the changes you made and the time you made them. You can then push these commits to the repository, where they are stored and tracked over time.

If a colleague also makes changes to the same file, Git will automatically detect the conflict and prompt you to resolve it. This way, you can ensure that everyone is working with the latest version of the code and that changes are integrated correctly.

With Git, you can also create branches, which allow you to work on different versions of the code simultaneously.

For example, you might create a branch to experiment with a new feature or fix a bug without affecting the main codebase. Once you are satisfied with the changes, you can merge the branch back into the main codebase.

Git makes it easy to track changes to your code, collaborate with others, and manage multiple versions of the same project files. It's a valuable tool for any developer working on a team project or even just for managing your own code over time.

## Understanding Commits

**A commit** is a snapshot of the changes you made to your code at a specific point in time. Each commit has a unique identifier, known as a `SHA-1` hash, which allows you to track and identify it. When you make a commit, Git records the changes you made and stores them in a repository.

Let's say you are working on a website project with a team of developers. You have just completed a task to update the website's header section to include a new logo and improved navigation menu.

Before you make any further changes to the code, you want to create a snapshot of the changes you made so that you can easily track and revert them if needed. This is where Git commits come in.

To create a commit, you first need to `add` the changes you made to the staging area. This is done by running the `git add` command on the modified files:

```bash
$ git add header.html
```

This tells Git to stage the changes you made to the header.html file. Once you have added all the changes you want to commit, you can create the commit using the `git commit` command:

```bash
$ git commit -m "Updated header section with new logo and improved navigation menu"
```

The commit message should describe the changes you made in a concise and meaningful way so that others can easily understand the purpose of the commit. In this case, the commit message clearly explains what was changed in the header section.

Once you have created the commit, Git will record the changes you made and store them in the repository. This creates a snapshot of the code at that particular point in time.

You can view the history of commits using the `git log` command, which shows all the commits made to the repository in reverse chronological order:

```bash
$ git log
commit 7f3d274b1c7ca9ba9f140c7a877a86fa4825de62 (HEAD -> master)
Author: John Doe <johndoe@example.com>
Date:   Tue Mar 8 15:00:00 2023 -0500
    Updated header section with new logo and improved navigation menu
commit aaf16df85e8e4d2856f24930c4e1a4f8dc2c7b9a
Author: Jane Doe <janedoe@example.com>
Date:   Mon Mar 7 14:00:00 2023 -0500
    Initial commit
```

In this example, the `git log` command shows the two commits that have been made to the repository, with the most recent one at the top. You can see the commit message and the author and date of each commit.

By understanding commits, you can easily track changes to your code over time and revert to previous versions if needed. This makes it easier to collaborate with others on a project and maintain a stable codebase.

## Understanding Branches

**A branch** is a separate line of development that allows you to work on different versions of your code simultaneously. When you create a branch, Git makes a copy of your code and allows you to make changes independently of the original branch.

This is useful when you want to experiment with new features or fix bugs without affecting the main codebase.

Let's say you are working on a web application project with your team, and you have just completed a major feature that adds a **new payment system** to the application.

However, before you merge your changes into the main codebase, you want to test the feature thoroughly and make sure it doesn't break anything else in the application.

This is where Git branches come in handy. A branch is a separate line of development that allows you to work on a copy of the codebase independently of the main codebase.

This means you can experiment with new features or make changes without affecting the main codebase until you are ready to merge them in.

To create a new branch, you use the git branch command followed by the name of the new branch:

```bash
$ git branch payment-system
```

This creates a new branch called **payment-system**, which is a copy of the current branch (in this case, the master branch). You can switch to the new branch using the git checkout command:

```bash
$ git checkout payment-system
```

Now you are working on the payment-system branch, which is a copy of the master branch at the time you created it. You can make changes to the code as usual, testing your new payment system thoroughly before committing your changes.

Once you are satisfied with the changes, you can merge the payment-system branch back into the master branch using the `git merge` command:

```bash
$ git checkout master
$ git merge payment-system
```

This takes all the changes you made on the payment-system branch and integrates them into the master branch, creating a new commit that combines the two branches.

By using branches, you can work on different features or make changes independently without affecting the main codebase until you are ready. This makes it easier to collaborate with others and maintain a stable codebase.

Additionally, branches allow you to easily test new features before integrating them into the main codebase, ensuring that they work as expected and don't break anything else in the application.

## Understanding Merges

**A merge** is a process of combining changes from one branch into another. When you merge a branch, Git combines the changes made in the branch with the original branch, creating a new snapshot of the code that includes both sets of changes.

**Example:**

Let us continue with the previous example of working on a web application project with a team and the new payment system feature on the payment-system branch.

Once you have tested the new feature thoroughly and are satisfied with it, you want to merge it back into the main codebase (master branch) so that everyone on the team can access and use it. This is where Git merges come in.

To merge the payment-system branch into the master branch, you first need to switch to the master branch using the git checkout command:

```bash
$ git checkout master
```

Then, you use the git merge command followed by the name of the branch you want to merge (payment-system in this case):

```bash
$ git merge payment-system
```

This integrates all the changes you made on the payment-system branch into the master branch, creating a new commit that combines the two branches.

However, there may be cases where conflicts arise during the merge process. For example, if someone else on the team made changes to the same lines of code on the master branch while you were working on the payment-system branch, Git may not be able to automatically merge the changes.

In this case, Git will mark the conflicting lines of code in the files with merge conflicts, and it's up to you to manually resolve the conflicts. You can do this by opening the files with conflicts and editing them to choose which changes to keep and which to discard.

Once you have resolved all the conflicts, you need to mark the conflicts as resolved using the `git add` command and then create a new commit to complete the merge:

```bash
$ git add .
$ git commit -m "Merged payment system feature from payment-system branch"
```

By understanding merges, you can easily integrate changes from different branches into the main codebase and collaborate with others on a project.

It also allows you to handle conflicts and ensure that the codebase remains stable and functional.

## Conclusion

Congratulations, you've made it to the end of the Git basics post! I hope that this post has helped you to understand the key concepts of [Git](https://git-scm.com/), and that you feel more confident using it in your projects.

Remember, Git is an incredibly powerful tool that can help you collaborate with others and manage your codebase more effectively. By mastering the basics of Git, you'll be well on your way to becoming a proficient developer.

But more importantly, I hope that you've enjoyed reading this post and that it has inspired you to keep learning and growing as a developer.

At the end of the day, programming is all about solving problems and making the world a better place, one line of code at a time. 

So keep coding, keep learning, and most importantly, keep dreaming big!