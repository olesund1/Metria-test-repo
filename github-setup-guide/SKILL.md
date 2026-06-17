---
name: github-setup-guide
description: Step-by-step guide for non-technical users to set up a GitHub repository and connect it to Claude Desktop. Use when someone wants to create a GitHub repo, set up version control, or needs guidance from zero to pushing code.
---

# GitHub Setup Guide for Claude Desktop

This skill guides you through setting up a GitHub repository and connecting it to Claude Desktop, even if you've never used GitHub or version control before.

## Before You Start

This guide assumes you have a code project or files you want to upload to GitHub. If you don't have a project yet, create a simple folder with some files (even a `README.txt` file is fine).

## The Journey Ahead

You'll go through these steps:
1. Set up a GitHub account (if you don't have one)
2. Install Git (if you don't have it)
3. Install Claude Desktop (if you don't have it)
4. Prepare your local project folder
5. Initialize Git in your project
6. Create a repository on GitHub
7. Connect your local project to GitHub
8. Push your code to GitHub
9. Verify everything is there

**Checkpoint:** At the end, you'll be able to see your code on GitHub, and Claude Desktop will have access to your project folder.

---

## Step 1: Do You Have a GitHub Account?

**Check:** Go to https://github.com and try logging in. If you can log in, skip to Step 2.

**If you don't have an account:**
1. Go to https://github.com
2. Click **Sign up**
3. Enter your email address
4. Create a password (something you'll remember)
5. Enter a username (this will be visible on GitHub — keep it professional)
6. Choose whether to receive updates (your choice)
7. Complete the verification (GitHub may ask you to verify you're human)
8. Check your email and verify your GitHub account

**Done?** Move to Step 2.

---

## Step 2: Do You Have Git Installed?

Git is the software that manages version control on your computer. Claude Desktop needs it.

**To check if you have Git:**

Open your computer's terminal/command line:
- **Mac:** Press `Cmd + Space`, type "Terminal", press Enter
- **Windows:** Press `Win + R`, type "cmd", press Enter

In the terminal, type:
```
git --version
```

**If you see a version number** (like "git version 2.40.0"), you already have Git. Skip to Step 3.

**If you get an error** or "command not found":

**On Mac:**
- Type this command: `xcode-select --install`
- A popup will appear. Click **Install** and wait for it to finish (this may take several minutes)
- When done, type `git --version` again to verify

**On Windows:**
- Download Git from https://git-scm.com/download/win
- Run the installer and follow the prompts (keep all default settings)
- Restart your terminal/command line
- Type `git --version` to verify

**Done?** Move to Step 3.

---

## Step 3: Do You Have Claude Desktop?

**Check:** Look for Claude Desktop on your computer. On Mac, check Applications. On Windows, check your Programs.

**If you don't have it:**
1. Go to https://claude.ai/download
2. Download Claude Desktop for your operating system
3. Run the installer and follow the prompts
4. Launch Claude Desktop

**Done?** Move to Step 4.

---

## Step 4: Prepare Your Project Folder

You need a folder on your computer with your code/files.

**Check:** Do you have a folder ready? For example:
- A folder called `my-project` with some code files
- Or `my-website` with HTML, CSS, and JavaScript files
- Or anything similar

**If you don't have one yet:**
1. Create a new folder on your computer (anywhere is fine — Desktop, Documents, etc.)
2. Name it something like `my-project`
3. Add some files to it (code files, README.txt, etc.)

**Important:** Remember the exact location of this folder — you'll need it later.

**Done?** Move to Step 5.

---

## Step 5: Initialize Git in Your Project

Now we'll tell Git to start tracking your project.

**Open your terminal/command line again** and navigate to your project folder:

**On Mac:**
```
cd /path/to/your/project
```
(Replace `/path/to/your/project` with the actual path. For example: `cd ~/Documents/my-project`)

**On Windows:**
```
cd C:\path\to\your\project
```
(Replace with your actual path. For example: `cd C:\Users\YourName\Documents\my-project`)

**Then type:**
```
git init
```

You should see a message like: "Initialized empty Git repository in /path/to/your/project/.git"

**Done?** Move to Step 6.

---

## Step 6: Create Your First Commit

Before connecting to GitHub, Git needs a "checkpoint" of your files.

**In the same terminal, type:**
```
git add .
```

This tells Git to track all your files.

**Then type:**
```
git commit -m "Initial commit"
```

This creates a checkpoint with the message "Initial commit". You should see output showing files being committed.

**Done?** Move to Step 7.

---

## Step 7: Create a Repository on GitHub

**Go to https://github.com and log in.**

1. Click the **+** icon in the top right corner
2. Select **New repository**
3. Give it a name (match your project folder name if possible, e.g., `my-project`)
4. Add a description (optional, but helpful)
5. Choose **Public** or **Private** (Public means anyone can see it; Private means only you can)
6. **Do NOT** check "Initialize this repository with a README" — you already have files locally
7. Click **Create repository**

**You'll see a page with setup instructions. Keep this page open — you'll need it next.**

**Done?** Move to Step 8.

---

## Step 8: Connect Your Local Project to GitHub

GitHub showed you some commands. Follow these steps:

**Copy this command from GitHub's instructions:**
```
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
```

(Replace `YOUR-USERNAME` with your GitHub username and `YOUR-REPO-NAME` with your repository name)

**Paste it into your terminal and press Enter.**

**Then type:**
```
git branch -M main
```

This ensures your main branch is called "main" (GitHub's default).

**Done?** Move to Step 9.

---

## Step 9: Push Your Code to GitHub

This is it — time to upload your code!

**In your terminal, type:**
```
git push -u origin main
```

**You may be asked to authenticate.** GitHub will open a browser window or ask for your credentials. Follow the prompts:
- If a browser opens, log in and authorize
- If asked for credentials, use your GitHub username and password (or a personal access token if you set one up)

**Wait for the upload to finish.** You should see output indicating files are being pushed.

**Done?** Move to Step 10.

---

## Step 10: Verify Everything is on GitHub

**Go to GitHub in your browser:**
1. Log in to https://github.com
2. Click your profile icon (top right)
3. Select **Your repositories**
4. Click on your new repository name

**You should see your files listed there!** If they're there, congratulations — you've successfully created a GitHub repository and pushed your code.

---

## Step 11: Connect Claude Desktop to Your Project

Now Claude Desktop can access your project for analysis and help.

**Open Claude Desktop:**
1. Launch Claude Desktop
2. Look for a way to add or connect a project/folder
3. Select your project folder (the one you've been working with)
4. Claude Desktop should now have access to your files

**You're done!** Your project is now:
- ✅ On your computer with Git tracking it
- ✅ On GitHub as a backup
- ✅ Connected to Claude Desktop for assistance

---

## Troubleshooting

**"Git command not found"** → Go back to Step 2 and install Git properly. Restart your terminal after installing.

**"Authentication failed"** → Make sure you're using the correct GitHub username and password. If you're having trouble, go to GitHub Settings → Developer Settings → Personal Access Tokens and create a token to use instead of your password.

**"Permission denied (publickey)"** → This usually means Git authentication is set up. Use the GitHub browser method when prompted for authentication.

**"Files not showing on GitHub"** → Check that your repository name matches what you created on GitHub. Try running `git push -u origin main` again.

**Can't find your project folder in the terminal?** → Use `pwd` (Mac) or `cd` without arguments (Windows) to see your current location, then navigate from there.

---

## Next Steps

Once everything is working:
- Make changes to your files locally
- Run `git add .` and `git commit -m "Description of changes"`
- Run `git push` to upload changes to GitHub
- Claude Desktop can help you with code questions about files in your project

**You've got this!** 🚀
