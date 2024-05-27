---
title: "How to Use the Integrated Terminal in VS Code"
datePublished: Mon May 27 2024 21:00:08 GMT+0000 (Coordinated Universal Time)
cuid: clwpgcu9q00040amq30gye5jf
slug: how-to-use-the-integrated-terminal-in-vs-code
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1716783688543/59a9538e-3790-4eca-b020-2877f6a16e6d.png
tags: terminal, vscode, vs-code, womenwhotech

---

Visual Studio Code (VS Code) is a powerful, versatile editor that many developers love. One of its standout features is the integrated terminal, which allows you to run command-line tools directly within the editor.

Whether you're new to VS Code or just looking to get more comfortable with its terminal, this step-by-step guide will help you make the most of this handy feature.

## Step 1: Open the Integrated Terminal

First things first, let's open the integrated terminal in VS Code. Here's how:

1. **Launch VS Code**: If you haven't already, open Visual Studio Code on your computer.
    
2. **Open the Terminal**: There are a few ways to do this:
    
    * **Using the Menu**: Go to the top menu and select `Terminal > New Terminal`.
        
    * **Using a Keyboard Shortcut**: Press `` Ctrl + ` `` (the backtick key, usually located below the `Esc` key).
        

**illustration**

%[https://youtu.be/Qc996k9RhJQ] 

That's it! You should see the terminal open up at the bottom of your VS Code window.

## Step 2: Configure the Terminal

VS Code allows you to customize the integrated terminal to suit your preferences. You can change the default shell, adjust the appearance, and more. Here's how you can tweak these settings:

### Change the Default Shell

By default, VS Code uses the default shell of your operating system. However, you can change this to any other shell, such as Git Bash, PowerShell, or Zsh.

1. **Open Settings**: Go to `File > Preferences > Settings` (or press `Ctrl + ,`).
    
2. **Search for Terminal Shell**: In the search bar, type "terminal shell".
    
3. **Edit the Shell Path**: Look for the `Terminal > Integrated: Shell` setting and update the path to your desired shell. For example:
    
    * **Git Bash**: `C:\\Program Files\\Git\\bin\\bash.exe`
        
    * **PowerShell**: `C:\\Windows\\System32\\WindowsPowerShell\\v1.0\\powershell.exe`
        
    * **Zsh** (on macOS): `/bin/zsh`
        

### Customize the Appearance

To make the terminal more visually appealing, you can change its font size, line height, and cursor style.

1. **Open Settings**: Again, go to `File > Preferences > Settings`.
    
2. **Search for Terminal Appearance**: Type "terminal font" or "terminal cursor" to find relevant settings.
    
3. **Adjust Settings**: Modify the settings as per your preference. For example, you can set the `Terminal > Integrated: Font Size` to 14 for a larger font.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716784703395/76bfdf05-5fed-4766-ac0d-8a35609960b6.png align="center")

## Step 3: Use Multiple Terminals

VS Code supports multiple terminals, which can be incredibly useful when you're working on different tasks simultaneously. Here's how to manage multiple terminals:

### Create a New Terminal

1. **Open a New Terminal**: Click the `+` icon in the terminal panel or select `Terminal > New Terminal` from the menu.
    
2. **Switch Between Terminals**: If you have multiple terminals open, you can switch between them using the dropdown menu in the terminal panel or by pressing `Ctrl + PageDown` and `Ctrl + PageUp`.
    

### Split the Terminal

You can also split the terminal to view multiple terminals side by side.

1. **Split the Terminal**: Click the split terminal icon in the terminal panel (looks like a split screen) or press `Ctrl + \`.
    
2. **Resize the Split Terminals**: Drag the separator between the split terminals to adjust their sizes.
    

%[https://youtu.be/Qc996k9RhJQ?si=5qAjv_r2zGlyO27d&t=26] 

## Step 4: Run Commands

Now that your terminal is set up, you can start running commands just as you would in any other terminal.

### Basic Commands

Here are some basic commands to get you started:

* **List Files**: `ls` (Linux/macOS) or `dir` (Windows)
    
* **Change Directory**: `cd <directory-name>`
    
* **Create a File**: `touch <file-name>` (Linux/macOS) or `type NUL > <file-name>` (Windows)
    
* **Remove a File**: `rm <file-name>` (Linux/macOS) or `del <file-name>` (Windows)
    

### Run a Program

If you're working on a project, you can run your programs directly from the terminal. For example, if you have a Python script, you can run:

```bash
python3 script.py
```

Or, if you're working on a Node.js project, you can run:

```bash
node app.js
```

## Step 5: Use Integrated Terminal Features

VS Code's terminal comes with several useful features to enhance your productivity.

### Terminal Links

When the terminal output contains links (like file paths or URLs), you can click them to open the corresponding file or webpage.

### Command History

Use the up and down arrow keys to navigate through your command history, allowing you to quickly rerun previous commands.

### Copy and Paste

You can easily copy and paste text in the terminal:

* **Copy**: Select the text and press `Ctrl + C`.
    
* **Paste**: Press `Ctrl + V`.
    

### Clear the Terminal

To clear the terminal screen, use the command:

```bash
clear
```

Or press `Ctrl + L` to achieve the same effect.

## Conclusion

I use the integrated terminal in VS Code because it is a powerful tool that can streamline your workflow by keeping everything in one place. With these steps, you should be well on your way to mastering the terminal and boosting your productivity. So, go ahead, give it a try, and happy coding!