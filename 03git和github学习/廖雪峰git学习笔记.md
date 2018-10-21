
# git使用笔记
[廖雪峰的git教程](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)学习笔记
#### windows 直接在 git 官网下载[下载地址](https://git-scm.com/downloads)，下载后在 Git Bash 配置 git
``` 
git config --global user.name "Your Name"
git config --global user.email "email@example.com"
#--global参数，表示你这台机器上所有的Git仓库都会使用这个配置，当然也可以对某个仓库指定不同的用户名和Email地址。
```
#### 创建目录，如果需要的话
``` 
git
mkdir learngit
cd learngit
pwd     
#pwd命令用于显示当前目录库
```
#### 通过 git init 命令把这个目录变成 Git 可以管理的仓库

```
git init
#通过git init命令把这个目录变成Git可以管理的仓库
```
#### add 和 commit文件
```
git add readme.txt
# 文件添加到仓库
git commit -m "wrote a readme file"
# 把文件提交到仓库,-m 后面输入的是本次提交的说明
git status
# 掌握仓库当前的状态
```

```
git diff readme.txt
git log
```



