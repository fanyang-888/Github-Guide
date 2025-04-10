# 更适合中国宝宝体质的Github指南

## 新手问题

### 什么是Github?

GitHub 是一个「代码仓库网站」，是程序员和开发者用来保存代码、记录变化、协作开发的地方。(如何保存，记录，更新会在下面讲到)

它是基于 Git (版本控制)这个工具的，但 Git 是本地用的，而 GitHub 是联网的、在线托管的。

### 怎么将代码保存到这个仓库？

你可以把你写的代码（项目文件夹）上传到 GitHub 上，存成一个叫“Repository（仓库）”的东西，就像你在你的百度网盘里放了一个文件夹，只不过这个文件夹里的文件可以实时修改并记录，还能和别人协作开发。

用 Git 工具你可以这样操作：

```
git init        # 在本地初始化一个 Git 仓库
git add .       # 添加所有文件
git commit -m "第一次提交"  # 提交修改
git push        # 推送到 GitHub 上

```

### 为什么要将代码、文件保存到GitHub上？

- 备份防丢（电脑坏了文件也不会丢失）
- 随时随地访问
- 和别人一起合作开发更方便
- 可以展示自己的项目给别人（找工作,申请学校加分）


### 什么是Git（版本控制）？

Git就像你写作业，每次都保存一个“版本”，这样哪怕后来出错，也可以「回到之前没错的版本」。

Git 就是这样的一个工具，它可以记录你每次提交修改的内容、时间、作者。

**你可以**：

- 回到之前的版本
- 比较修改了哪些地方
- 多人一起工作，不用担心互相覆盖

**为什么重要？**

如果你只是自己做项目，可能觉得没啥。但你做久了就会发现：

- 一不小心改错了，想回到原来版本
- 项目越做越大，需要记录每一步做了什么
- 多人合作时必须知道谁改了什么

### 为什么可以协作开发？不会互相冲突吗？

**Git + GitHub 怎么协作？**

- 每个人可以创建自己的分支（branch），在上面修改代码
- 修改完后提交一个 Pull Request，团队审核通过后合并进主分支
- Git 会自动尝试把不同人的代码合在一起，如果冲突了，就提示你解决冲突（不会强行挤出去）

### Git 和 GitHub 的区别？

| 比较       | Git                         | GitHub                                 |
|------------|------------------------------|------------------------------------------|
| 本质       | 版本控制工具                | 在线协作平台（托管 Git 仓库）           |
| 使用方式   | 命令行/本地工具             | 网页 + Git 客户端                       |
| 是否联网   | 不需要联网                  | 需要联网                                |
| 功能       | 追踪代码变化、版本管理      | 团队协作、Issue 追踪、Pull Request 等   |

> 💡 Git 更像是“保存和管理代码”的工具，GitHub 是“展示和协作代码”的地方。


**❗ 如果两个人同时修改了同一段代码？**

Git 会提示有冲突（conflict），你就得手动选择保留哪一部分。 但只要不是同时改同一行，就能自动合并。

## 开始使用GitHub

### 注册账号

- 打开 https://github.com
- 点击右上角 Sign up（注册）
- 填写邮箱、用户名、密码并验证邮箱
- 选择免费方案，即可开始使用

### 在电脑中下载GitHub

- 官网：https://desktop.github.com/download/
- 下载对应电脑版本即可

### GitHub 基本界面介绍

- Repositories（仓库）：你的项目/代码文件夹
- Issues：用来追踪 Bug、建议、任务等（像待办清单）
- Pull Requests（PR）：提交代码修改请求（用于多人协作）
- Actions：自动化工具，可用来运行测试、部署等

其他常见模块：
- Stars：你可以给喜欢的项目点星标
- Fork：复制别人的仓库来修改
- Watch：关注项目更新

### 创建你的第一个仓库（Repository）

- 登录后点击右上角 + → New Repository![image](https://github.com/user-attachments/assets/96847cea-ef9a-4d7f-bb9d-0cd5ee707f6c)
- 写项目名称（比如：我想创造一个黄焖鸡菜谱，起名黄焖鸡）
- 可以选择添加 README 文件（建议勾选）
- 设置为 Public（公开）或 Private（私有）![image](https://github.com/user-attachments/assets/2be0d898-c731-432a-a48c-e1ec5c5c6599)
- 点击 Create Repository 创建完成![image](https://github.com/user-attachments/assets/0b421607-5326-4f23-9598-69f946b56723)

### README 文件的作用和写法

README.md 是每个仓库的门面，是别人了解你项目的第一入口。

应包含：项目简介、安装说明、使用方法、贡献指南、许可证（License）。加上截图、Demo 链接更吸引人！

## 使用git管理电脑上的项目

### 施工中

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


| Miner Model                  | Price (USD) | Algorithm           | Daily Profit* | Power   | Efficiency  | Recommended For                          |
|-----------------------------|-------------|---------------------|----------------|---------|-------------|------------------------------------------|
| Bitmain Antminer S21 Pro    | $4900       | SHA256 (BTC)        | $1.60          | 3550W   | ~21 J/TH    | High performance & stability for BTC     |
| iPollo G1                   | $4599       | CKB (Eaglesong)     | $8.24          | 2800W   | -           | High profit, ideal for professional farms |
| Bitdeer Sealminer A2 Pro Air| $4100       | SHA256              | $1.83          | 3400W   | -           | Excellent cooling & low noise            |
| Bitmain Antminer S21        | $3700       | SHA256              | $0.17          | 3500W   | -           | Trusted brand, good resale value         |
| FLUMINER-L1                 | $3199       | Scrypt (LTC+DOGE)   | $2.07          | 2900W   | -           | Dual-mining support, home-friendly       |

