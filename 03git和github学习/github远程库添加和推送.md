### 创建密钥对
- 创建SSH Key。
- 登陆GitHub，打开“Account settings”，“SSH Keys”页面：
然后，点“Add SSH Key”，填上任意Title，在Key文本框里粘贴id_rsa.pub文件的内容
```
ssh-keygen -t rsa -C "youremail@example.com"
#在用户主目录里找到.ssh目录，里面有id_rsa和id_rsa.pub两个文件，这两个就是SSH Key的秘钥对，id_rsa是私钥，不能泄露出去，id_rsa.pub是公钥，可以放心地告诉任何人
```

为什么GitHub需要SSH Key呢？因为GitHub需要识别出你推送的提交确实是你推送的，而不是别人冒充的，而Git支持SSH协议，所以，GitHub只要知道了你的公钥，就可以确认只有你自己才能推送。

当然，GitHub允许你添加多个Key。假定你有若干电脑，你一会儿在公司提交，一会儿在家里提交，只要把每台电脑的Key都添加到GitHub，就可以在每台电脑上往GitHub推送了。

### 添加远程库github
首先在github新建一个项目，然后把这个项目地址复制下来，添加远程库
```
git remote add origin git@github.com:michaelliao/learngit.git
```
把本地库的所有内容推送到远程库
```
git push -u origin master
# 第一次提交，-u参数，Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令。

git push origin master
# 当前分支master推送到远程origin，
```

## 小结
- 要关联一个远程库，使用命令git remote add origin git@server-name:path/repo-name.git；

- 关联后，使用命令git push -u origin master第一次推送master分支的所有内容；

- 此后，每次本地提交后，只要有必要，就可以使用命令git push origin master推送最新修改；



