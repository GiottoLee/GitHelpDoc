# Git使用教程

## **配置Git**

- ### git --version &emsp;查看Git版本
> PS G:\DOC> git --version  
git version 2.21.0.windows.1

<br/>

- ### git comnfig --global user.name "GiottoLee" &emsp;配置全局用户名

- ### git comnfig --global user.email "xxx@outlook.com" &emsp;配置全局用户名

- ### git comfig --list &emsp; 查看当前所有项目

> PS G:\DOC> git config --list  
    core.symlinks=false  
    core.autocrlf=true  
    core.fscache=true  
    color.diff=auto  
    color.status=auto  
    color.branch=auto  
    color.interactive=true  
    help.format=html  
    rebase.autosquash=true  
    http.sslbackend=openssl  
    http.sslcainfo=F:/Git/mingw64/ssl/certs/  ca-bundle.crt  
    credential.helper=manager  
    user.name=GiottoLee  

<br/>

## **创建仓库**

- ### git init &emsp; 初始化仓库
> PS G:\DOC\GitDoc> git init  
Reinitialized existing Git repository in G:/DOC/GitDoc/.git/

- ### git clone [ *连接* ] &emsp； 克隆仓库

<br/>

## **基本用法**

- ### git status &emsp; 查看状态
>PS G:\DOC\GitDoc> git status  
On branch master  
No commits yet  
Untracked files:  
  (use "git add <file>..." to include in what will be committed)  
        "Git\344\275\277\347\224\250\346\225\231\347\250\213.md"  
nothing added to commit but untracked files present (use "git add" to track)  

- ### git add . &emsp;将所有修改添加至暂存区