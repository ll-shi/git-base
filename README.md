# git常用操作

git是把代码从远程仓库克隆到本地的git仓库，然后从本地仓库checkout(检出)

    在提交之前先将代码提交到暂存区，

    确认提交之后。将代码提交到本地仓库。本地仓库中保存着修改着的各个历史版本。

    最后需要把本地仓库的代码push到远程仓库。

    本地库初始化

    首先在项目目录下面进行git的初始化 git init 然后这个文件夹就是git中的一个仓库了。

     
    第二个设置签名：就相当在你写的代码上签上你的名字。

    在仓库目录执行命令
    
    所以我们就要设置签名

    注意点：这里的签名跟我们把代码推到远程仓库的账号不一样。远程账号就是为了推代码。签名就是给我们的代码提供签名

    签名分类：1.项目签名 如果两种签名都有，项目签名有效。

     git config user.name 用户名

     git config user.email 邮箱名

     git config user.name llshi

     git config user.email Light.Winstones@gmail.com

    2. 系统级别签名
    
    git config --global user.name

    git config --global user.email

    二者都没有是不允许的。（提交的代码必须要有签名）

    3. 配置文件位置当前仓库 .git/config 文件中


    使用git add 把文件添加到暂存区。就相当vscode中的加号一样，添加到暂存区。

    git rm --cache 文件名 把文件从暂存区删除。

    git status 查看git状态。(非常常用的一个命令)

    git log 查看日志 历史提交

    git log --oneline 日志只显示一行，前面的哈希值就相当版本号。 head指向当前版本

    git reflog 推荐使用

    控制历史版本的前进后退。

    从远程库克隆到本地库。不是成员就克隆，是项目成员叫拉取

    使用git remote 来查看远程仓库

    使用 git remote add 来添加远程仓库可以使用别名

    git remote add 别名 url

    使用 git remote rm 别名 来删除远程仓库。

    使用 git ls-files 来查看git仓库中有哪些文件。

    删除本地git 文件 git rm -r 文件夹。

    使用git clone 链接 克隆代码

    git clone https://github.com/ll-shi/vue.git (注意不要写别名)

    切换分支：git checkout -b

    git clone 跟git pull区别。git clone是将这个仓库中的代码都下载下来。

    git pull 是拉取远程仓库中更新的代码，并且跟本地代码进行合并。

    git push

    分支相关

    查看分支 git branch

    切换分支 git checkout 分支名

    创建新分支 git branch name

    创建并且切换分支 git checkout -b name

    删除远程分支 git push origin --delete 分支名

    删除本地分支 git branch -D 分支名

    合并分支：

    创建仓库的完成过程。

    1. 创建远程仓库。并添加一个readme.md文件。如果仓库中什么文件都没有，也会报错。

    2. 在终端中使用git clone 把远程仓库clone下来，然后设置签名，导入到vscode中。配置远程仓库。

    3. 创建并切换分支。一般我们从远程仓库倒下来都建一个自己的分支。方便后续操作。git checkout -b '分支名'

    4. 把修改文件提交到git暂存区 git add .
    
    5. 把暂存区文件提交到git仓库 git commit -m "描述信息"

    6. 推到远程仓库 git push 远程仓库地址(vue，这是一个远程仓库地址别名) 本地分支名（'1.课程准备'，这是一个分支名）

    7. 下次添加新的内容的时候，创建一个新的分支并切换。 然后开始添加新的内容

## git 版本回退

1）首先在commit中复制hard版本号
2）使用 git reset --hard 版本号
3）使用 git push -f 强制提交

### .gitignore文件

1）用来制定不跟踪的文件或者文件夹。
