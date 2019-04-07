# Git使用教程

## **配置Git**

- ### git --version &emsp;查看Git版本
```
PS G:\DOC> git --version  
git version 2.21.0.windows.1
```

<br/>

- ### git comnfig --global user.name "GiottoLee" &emsp;配置全局用户名

- ### git comnfig --global user.email "xxx@outlook.com" &emsp;配置全局用户名

- ### git comfig --list &emsp; 查看当前所有项目

```
PS G:\DOC> git config --list  
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
```

<br/>

## **创建仓库**

- ### git init &emsp; 初始化仓库
```
PS G:\DOC\GitDoc> git init  
Reinitialized existing Git repository in G:/DOC/GitDoc/.git/
```

- ### git clone [ *连接* ] &emsp； 克隆仓库

<br/>

## **基本用法**

- ### git status &emsp; 查看状态
```
PS G:\DOC\GitDoc> git status  
On branch master  
No commits yet  
Untracked files:  
  (use "git add <file>..." to include in what will be committed)  
        "Git\344\275\277\347\224\250\346\225\231\347\250\213.md"  
nothing added to commit but untracked files present (use "git add" to track)  
```

- ### git add . &emsp;将所有修改添加至暂存区
```
PS G:\DOC\GitDoc> git add .
```

- ### git add [*File name*] &emsp;将指定文件添加至暂存区
~~~
PS G:\DOC\GitDoc> git add HowToUseGit.md
~~~

- ### git commit -m "*备注*" &emsp; 提交版本
```
PS G:\DOC\GitDoc> git commit -m "Contribute how to use Git tools."
[master (root-commit) 3ccc1ff] Contribute how to use Git tools.
 1 file changed, 55 insertions(+)
 create mode 100644 "Git\344\275\277\347\224\250\346\225\231\347\250\213.md"
```

- ### git log &emsp; 查看历史版本
```
PS G:\DOC\GitDoc> git log
commit 3ccc1ff91f3e2a6f9ed5908f414717893d9e3928 (HEAD -> master)
Author: GiottoLee <giottolee@outlook.com>
Date:   Sun Apr 7 21:17:44 2019 +0800

    Contribute how to use Git tools.
```

- ### git log -p &emsp; 查看历史版本附加详细信息
~~~
PS G:\DOC\GitDoc> git log -p
commit 3ccc1ff91f3e2a6f9ed5908f414717893d9e3928 (HEAD -> master)
Author: GiottoLee <giottolee@outlook.com>
Date:   Sun Apr 7 21:17:44 2019 +0800

    Contribute how to use Git tools.

diff --git "a/Git\344\275\277\347\224\250\346\225\231\347\250\213.md" "b/Git\344\275\277\347\224\250\346\225\231\347\250\213.md"
new file mode 100644
index 0000000..dc41cd9
--- /dev/null
+++ "b/Git\344\275\277\347\224\250\346\225\231\347\250\213.md"
@@ -0,0 +1,55 @@
+# Git使用教程
+
+## **配置Git**
+
+- ### git --version &emsp;查看Git版本
+> PS G:\DOC> git --version  
+git version 2.21.0.windows.1
+

...

+
+- ### git add . &emsp;将所有修改添加至暂存区
\ No newline at end of file
~~~


- ### git status &emsp; 查看当前状态
```
PS G:\DOC\GitDoc> git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   "Git\344\275\277\347\224\250\346\225\231\347\250\213.md"

no changes added to commit (use "git add" and/or "git commit -a")
```

- ### git checkout *版本号* &emsp; 穿越到指定的历史节点
```
PS G:\DOC\GitDoc> git checkout f921330
```

- ### git checkout - &emsp; 回到上一个版本节点
~~~
PS G:\DOC\GitDoc> git checkout -
~~~

<br/>

## **三种状态**

1. Modified &emsp； 修改状态
2. Staged &emsp; 暂存状态
3. Committed &emsp; 提交状态

<br/>

## **标签Tag**

- ### git tag -a [*标签名*] -m "*备注*"