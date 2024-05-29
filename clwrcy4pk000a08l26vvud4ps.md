---
title: "How to Handle Large Files in GitHub Repositories?"
datePublished: Wed May 29 2024 05:00:15 GMT+0000 (Coordinated Universal Time)
cuid: clwrcy4pk000a08l26vvud4ps
slug: how-to-handle-large-files-in-github-repositories
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1716785936761/219a6cb3-fd23-4393-8f27-a94591b5708e.png
tags: github, womenwhotech, github-large-files, handling-large-files-on-github

---

Hey there! If you’ve ever tried to push large files to your GitHub repository, you might have run into a few hiccups.

GitHub has a strict file size limit, which can be quite frustrating when you need to manage large assets like datasets, videos, or high-resolution images.

Let’s dive into a step-by-step guide on how to hangithubdle large files in GitHub repositories smoothly.

## Step 1: Understand GitHub's File Size Limits

First things first, it’s crucial to understand GitHub’s file size limits:

* Individual files in a repository can be up to 100 MB.
    
* The total repository size can be up to 1 GB.
    
* If you need to handle files larger than 100 MB, you’ll need to use Git Large File Storage (LFS) or other workarounds.
    

## Step 2: Install Git Large File Storage (LFS)

Git LFS is an extension for Git that allows you to manage large files by storing them outside your Git repository while keeping pointers to them in your repo. Here’s how to set it up:

1. **Install Git LFS**:
    
    * On Windows: Use the installer from [git-lfs.github.com](http://git-lfs.github.com).
        
    * On macOS: Use Homebrew by running `brew install git-lfs`.
        
    * On Linux: Use your package manager, e.g., `sudo apt-get install git-lfs`.
        
2. **Initialize Git LFS**:
    
    ```sh
    git lfs install
    ```
    
3. **Track Large Files**: You need to specify which files to track with LFS. For example, to track all `.psd` files:
    
    ```sh
    git lfs track "*.psd"
    ```
    
4. **Add the Changes to Git**:
    
    ```sh
    git add .gitattributes
    ```
    

## Step 3: Commit and Push Large Files

Once Git LFS is set up, you can commit and push large files just like any other files:

1. **Add Your Files**:
    
    ```sh
    git add path/to/large-file.ext
    ```
    
2. **Commit the Changes**:
    
    ```sh
    git commit -m "Add large file"
    ```
    
3. **Push to GitHub**:
    
    ```sh
    git push origin main
    ```
    

## Step 4: Verify Your Large Files on GitHub

After pushing your files, you can verify that Git LFS is correctly handling them:

1. **Check the File in Your Repository**: Navigate to your repository on GitHub and check the file. It should display as a pointer file, not the actual large file content.
    
2. **Verify the File Size**: The file size on GitHub should match the size before uploading. If it exceeds 100 MB and was successfully pushed, Git LFS is working correctly.
    

## Step 5: Managing and Cleaning Up Large Files

Occasionally, you might need to manage or remove large files from your repository to keep it clean and within limits.

1. **Removing Large Files**: To untrack a file and remove it from the repository, you need to use:
    
    ```sh
    git rm --cached path/to/large-file.ext
    git commit -m "Remove large file"
    git push origin main
    ```
    
2. **Garbage Collection**: To clean up your local repository, run:
    
    ```sh
    git gc
    ```
    

## Step 6: Alternative Solutions for Handling Large Files

If Git LFS isn't a fit for your needs, consider these alternatives:

1. Use services like Amazon S3, Google Drive, or Dropbox to store large files and link to them in your repository.
    
2. Split large files into smaller chunks that are within GitHub’s size limits and store them in the repository. Use a script to reassemble them when needed.
    
3. Create a separate repository specifically for large files and use Git submodules to link it to your main repository.
    

## Conclusion

Handling large files in GitHub doesn’t have to be a headache. With Git LFS and a few best practices, you can efficiently manage large assets in your repositories.

Happy coding!

Do you have any questions or need further help? Drop a comment below or reach out to me on [Twitter(X](https://x.com/fanny_codes)).