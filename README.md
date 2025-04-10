# 更适合中国宝宝体质的Github指南

## 新手问题

### 什么是Github?

GitHub 是一个「代码仓库网站」，是程序员和开发者用来保存代码、记录变化、协作开发的地方。(如何保存，记录，更新会在下面讲到)

它是基于 Git 这个工具的，但 Git 是本地用的，而 GitHub 是联网的、在线托管的。

## Basic

### Download GitHub 

Download GitHub in your laptop, go to official website: https://desktop.github.com/download/

### Get Started

Open your terminal

To check which version of git is installed, `git --version`

### Configure Git - Let GitHub know who you are
Set the user name for the current repository to "w3schools-test": `git config user.name "w3schools-test"`

Set the user email for the current repository to "xxx@gmail.com": `git config --global user.email "xxx@gmail.com"`

### Creating Git Folder

`mkdir` makes a new directory: `mkdir myproject`

`cd` changes the current working directory: `cd myproject`

Initialize Git on the current folder: `git init`

Check the status of the Git: `git status`

### Git files

`ls` will list the files in the directory.

### Git Staging Environment

Add file `index.html` to staging environment: `git add index.html`

Add all files in the current directory to the Staging Environment: `git add --all`

Stage all new, modified, and deleted files: `git add -A`

### Git commit

After finishing out project, we need to remove from stage to commit: `git commit -m "message"`

Check the status of repository, see the changes in a more compact way: `git status --short`

Commit the updated files directly, skipping the staging environment: `git commit -a -m`

To view the history of commits for a repository, you can use the `log` command: `git log`

### Git help

`git command -help` -  See all the available options for the specific command

`git help --all` -  See all possible commands

### Git branch

A branch is a new/separate version of the `main` repository.

Without Git:
- Make copies of all the relevant files to avoid impacting the live version
- Start working with the design and find that code depend on code in other files, that also need to be changed!
- Make copies of the dependant files as well. Making sure that every file dependency references the correct file name
EMERGENCY! There is an unrelated error somewhere else in the project that needs to be fixed ASAP!
- Save all your files, making a note of the names of the copies you were working on
- Work on the unrelated error and update the code to fix it
- Go back to the design, and finish the work there
- Copy the code or rename the files, so the updated design is on the live version
- (2 weeks later, you realize that the unrelated error was not fixed in the new design version because you copied the files before the fix)

With Git:
- With a new branch called new-design, edit the code directly without impacting the main branch
- EMERGENCY! There is an unrelated error somewhere else in the project that needs to be fixed ASAP!
- Create a new branch from the main project called small-error-fix
- Fix the unrelated error and merge the small-error-fix branch with the main branch
- You go back to the new-design branch, and finish the work there
- Merge the new-design branch with main (getting alerted to the small error fix that you were missing)


