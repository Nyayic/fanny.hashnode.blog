---
title: "How to Enable Spell Check in VS Code?"
datePublished: Sun Jun 02 2024 05:00:26 GMT+0000 (Coordinated Universal Time)
cuid: clwx2psa6000109jq3na16kbo
slug: how-to-enable-spell-check-in-vs-code
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1716787972611/4f63f49b-97a1-4446-b3c2-3e061fda9030.png
tags: visual-studio, vscode, vs-code, womenwhotech

---

If you're like me, you probably spend a good chunk of your day typing away in Visual Studio Code (VS Code). It's an amazing tool for coding, but let’s face it—sometimes our spelling can be a bit off, especially when we’re writing comments, documentation, or even commit messages. Luckily, VS Code has got us covered with a spell-check feature!

## How to Enable Spell Check in VS Code

### Step 1: Install the Spell Check Extension

First things first, we need to install an extension that provides spell checking. One of the most popular and effective extensions for this purpose is "Code Spell Checker".

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716804051025/824ef55e-b283-4066-857f-83584606a9e3.png align="center")

1. **Open VS Code**.
    
2. **Go to the Extensions View** by clicking on the Extensions icon in the Activity Bar on the side of the window. You can also open it by pressing `Ctrl+Shift+X` on Windows/Linux or `Cmd+Shift+X` on macOS.
    
3. **Search for "Code Spell Checker"** in the search bar.
    
4. **Click Install** to add the extension to your VS Code.
    

### Step 2: Configure the Extension

Once you have the "Code Spell Checker" installed, you'll need to configure it to suit your needs.

1. **Open the Command Palette** by pressing `Ctrl+Shift+P` on Windows/Linux or `Cmd+Shift+P` on macOS.
    
2. **Type "Preferences: Open Settings (JSON)"** and select it. This will open the settings.json file where you can manually add configurations.
    
3. **Add Configuration Settings**. You can customize various settings such as the language of the spell checker, which files and folders to include or exclude, and more. Here’s an example configuration:
    
    ```json
    {
        "cSpell.language": "en",
        "cSpell.enabled": true,
        "cSpell.excludePaths": [
            "**/node_modules/**",
            "**/dist/**"
        ],
        "cSpell.words": [
            "someCustomWord",
            "anotherCustomWord"
        ]
    }
    ```
    
    * `"cSpell.language": "en"` sets the spell checker to English.
        
    * `"cSpell.enabled": true` enables the spell checker.
        
    * `"cSpell.excludePaths"` lets you specify which folders to ignore.
        
    * `"cSpell.words"` allows you to add custom words that are specific to your project.
        

### Step 3: Using the Spell Checker

Now that the spell checker is enabled and configured, you can start using it!

* **Misspelled words will be underlined** with a squiggly line, similar to how a traditional spell checker works.
    
* **Right-click on the underlined word** to see suggestions for corrections.
    
* **Add words to your personal dictionary** by selecting “Add to Workspace Dictionary” or “Add to User Dictionary” if the word is correct but not recognized by the spell checker.
    

### Bonus Tips

* If you code in multiple languages, you can add language packs to the "Code Spell Checker" extension. For example, if you need French, search for "Code Spell Checker French" in the Extensions view.
    
* You can configure the spell checker to ignore certain words or patterns by adding them to your settings.json file.
    
    ```json
    {
        "cSpell.ignoreWords": [
            "ignoreThisWord"
        ],
        "cSpell.ignoreRegExpList": [
            "/^\\s*#/"
        ]
    }
    ```
    
    * `"cSpell.ignoreWords"` lets you ignore specific words.
        
    * `"cSpell.ignoreRegExpList"` allows you to ignore text that matches specific regular expressions.
        

And there you have it! Enabling and configuring spell check in VS Code is a straightforward process that can save you from those embarrassing typos. Whether you’re writing code comments, documentation, or commit messages, a spell checker is a handy tool to ensure your text is error-free.

Happy coding and spelling!