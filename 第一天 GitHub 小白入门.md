# 第一天 GitHub 小白入门

## Git是一个分布式版本控制系统。GitHub 是通过 Git 进行版本控制的软件源代码托管服务平台。

## 登录之后第一排

- **Pull requests**：你想参与别人的项目，或想改进别人的项目，改进后需要提交申请，用 pull requests。
- **Repository：**翻译为仓库，也是你的项目。你可以理解成一个大的文件夹，或者笔记本。一个项目对应一个 Repository。
- **Issues**：你发现别人项目的 bug，或者有什么问题，怎么和作者交流呢？提一个 Issue ；别人也可以给你的项目提 Issue 反馈问题。Issue 追踪各种想法，增强功能，任务，bug，有点儿像评论功能。
- **Marketplace**：应用商店，里面有免费/收费的开发工具。
- **Explore**：你可以理解成软件里的发现页，点进去推荐一些和你相关的话题、项目、新闻等。

**网页中间**:是你关注的人的动态，比如他给别人点赞，他又建了一个项目。

**网页右边**:类似于推荐页，网站根据你的喜好推荐一些相关项目。

## 个人界面

右上角那个头像就是**个人界面** 

**Settings** 可以更改你的资料

**Your profile** 就可以进入你的主页

- **Projects**：它可不是项目，上面说了 Repository 是项目。它可以翻译为项目板，是 project-boards 的简写， 通过项目板可以灵活地创建适合需求的自定义工作流程，说白了是管理项目流程的，一般不常用。

- **Star**：就是点赞功能，这里用作动词，它叫 star 是因为点赞图标就是星星⭐。不过这个点赞比较像知乎里的点赞功能，它会记录在你的动态里。由于 GitHub 没有收藏功能，所以 star 可以用来收藏。

- **Follow**：就是关注的意思，点击 Followers 看看谁关注了他，点击 Following 看看他关注了谁（大神关注的一般也是大神 ）

## 项目界面

- **Watch**：关注观察 ，也就是你既可以关注（follow）一个人，也可以关注（watch）一个项目，你关注内容的动态都会显示在主页面。

- **Fork**：直译是刀叉，它是指将 GitHub 的某个特定仓库（所有文件）原封不动地复制到自己的账户下。比如你想改进这个项目，加点儿自己的东西，就可以复制一下整个仓库再修改，但是不影响原作者的仓库，你点击 Fork 就能复制。

下面一条是标签页，比如默认的一个标签页 .**Code** 就是展示代码的页面；如果你想看别人提的问题就点击. **Issues** 页，也许你遇到的问题别人提过并且解决了；有的人想参与这个项目，他改好后就向作者发起了. **Pull Requests**，希望作者接受他的改进，点进去可以看谁提交过什么样的改进，作者是否采纳。**Clone or downloads** 下载到本地.

**Git：**上面没有提到，但是主界面点击头像可以看到 Your Gist。如果你没有一个项目，只是单纯地想分享一些代码片段，就可以写 Gist。

**README.md：**每当创建项目、初始化时，都会帮你自动生成 README.md 文件并显示在仓库首页。一般都是使用 Markdown 语法（准确来说应该是GitHub Flavored Markdown(GFM）语法)来描述项目的概要、使用流程、许可协议等。

## Git安装使用

**git status** 命令，查看仓库状态。

**git init** 初始化，可以看到初始化完成，它是一个空的 Git 仓库。

输入 **git add test.txt**我们往仓库里添加文件，再输入 **git status** 看看仓库状态.

- **git commit -m “message”**，-m 参数表示可以直接输入后面的 “message” ，如果不加 -m 参数，那么是不能直接输入 message的，而是会调用一个编辑器一般是 vim 来让你输入这个 message。

- **git commit -a -m “massage”**，加的 -a 参数可以将**所有**已跟踪文件中的执行修改或删除操作的文件都提交到本地仓库，即使它们没有经过 git add 添加到缓存区，注意，新加的文件（即没有被 git 系统管理的文件）是不能被提交到本地仓库的。建议一般不要使用 -a 参数，正常的提交还是使用 git add 先将要改动的文件添加到暂存区，再用 git commit 提交到本地版本库。

- **git commit --amend**，追加提交，它可以在不增加一个新的commit-id的情况下将新修改的代码追加到前一次的commit-id中

输入 **git log** 命令，打印 Git 仓库提交日志，会显示作者、时间和你写的提交信息

## GitHub下载提交代码

某个项目的界面的 **Clone or download** 按钮可以下载整个仓库/项目的文件。输入 **git clone**，后面跟项目的 URL,如:git clone https://github.com/project/repo.git   git clone git@github.com:project/repo.git

```text
git push origin main # 把本地代码推到远程 main 分支
git pull origin main # 把远程最新的代码更新到本地
```

**一般我们在 push 之前都会先 pull ，这样不容易冲突。**

如果已经发生冲突,考虑git pull/push origin 分支名 --rebase/--force

**在`git add` 之前**使用 `git diff` 可以显示你对某一文件的改动.

```text
git reset --hard 版本号 (抛弃当前工作区的修改)
git reset --soft 版本号 (回退到之前的版本，但保留当前工作区的修改，可以重新提交)
```

 
