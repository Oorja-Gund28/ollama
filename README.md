Here's a comprehensive beginner-friendly tutorial for your students covering Git and GitHub fundamentals, tailored for both Windows PC and Mac, with usage in Cursor, working in Python notebooks/modules, and using uv for package management.

🧠 Git and GitHub 101: Self-Study Guide
📦 Part 1: What is Git? (Purpose and Background)

Git is a version control system (VCS). Think of it as a time machine for your code.

🧾 What it does:
Tracks changes to your files over time.
Lets you revert to previous versions.
Helps teams collaborate without stepping on each other's toes.
📚 Background:
Created by Linus Torvalds in 2005 (yep, the same guy who made Linux).
Designed to be fast, distributed, and safe.
Now an industry standard for managing software projects.
✅ Why You Should Care:

When you're editing code — whether it's a .py module or a .ipynb notebook — Git helps you:

Save your work as snapshots.
See what changed and when.
Avoid "oops I broke everything" moments.
Work smoothly with others.
🛠️ Exercise 1: Installing Git

Mac:

brew install git

(Or install Xcode command line tools when prompted.)

Windows:

Download Git from https://git-scm.com/download/win
Run the installer with default settings.

Then open Terminal (Mac) or Git Bash / Command Prompt (Windows) and run:

git --version

You should see something like:

git version 2.44.0
🛠️ Part 2: Basic Git Commands

Let’s simulate saving your work like checkpoints in a game:

🧩 git status

Shows you what’s changed, what’s saved, and what’s still pending.

git status

You’ll often see:

Modified files
Untracked files (new files not yet added)
Which branch you’re on
➕ git add

Tells Git, “Hey, I want to include this file in the next save.”

git add my_script.py

Or add everything:

git add .
💾 git commit

This saves the changes you’ve added. You must include a message describing your update.

git commit -m "Add new analysis for customer churn"

That commit is now a snapshot in Git’s history!

🛠️ Exercise 2: Your First Commit
Create a new folder and a Python file or notebook inside:
mkdir git-demo
cd git-demo
echo "print('Hello world')" > hello.py
Initialize Git:
git init
Run:
git status
git add hello.py
git commit -m "Initial commit with hello script"

🎉 You've now committed your first file!

☁️ Part 3: What is GitHub? (And how is it different from Git?)

Git = Version control on your own machine.

GitHub = Online service to store, share, and collaborate on Git projects.

🔍 Key Differences:
Git	GitHub
Runs locally	Cloud-based
Manages versions	Hosts code + project tools
Command-line tool	Website UI & API
No login needed	Login required
💡 Alternatives to GitHub:
GitLab (open-source, often self-hosted)
Bitbucket (popular with teams using Jira/Atlassian)
SourceHut, Gitea (lightweight alternatives)
🛠️ Exercise 3: Create a GitHub Account
Go to https://github.com
Sign up and verify your email.
Create a new repository, call it demo-repo.
📥 Part 4: What Does git clone Do?

When you see a GitHub repo and want to work with it locally:

git clone https://github.com/username/demo-repo.git
What It Does:
Downloads all files and commit history.
Sets up the .git folder for local version tracking.
Adds a link to GitHub as the origin remote, so you can later pull/push.
🛠️ Exercise 4: Clone a Repo

Clone your own repo:

git clone https://github.com/YOUR_USERNAME/demo-repo.git
cd demo-repo

Make a small change to any file, and run:

git status
🔁 Part 5: git pull and git push (Intro)

These commands sync your local repo with the remote one on GitHub.

🔄 git pull

Fetches the latest changes from GitHub into your local repo.

git pull origin main
⬆️ git push

Sends your local commits up to GitHub.

git push origin main

📝 Note: You’ll learn detailed usage of pull/push with your course repo in a separate guide.

🛠️ Exercise 5: Make a Change and Push
Edit hello.py to print your name.
Run:
git status
git add hello.py
git commit -m "Add my name to hello script"
git push origin main
Go to your GitHub page — you’ll see your change online!
✅ Wrap-up

You’ve now learned:

What Git and GitHub are
Key Git commands to track and save work
How GitHub connects to your local work
How to clone a repo and sync changes
🧪 Optional Challenge
Create a new Python project.
Initialize Git, make several commits.
Push it to a new GitHub repo.
Clone it to a different folder and test pulling/pushing.
