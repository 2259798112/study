元数据

`>` 替换
`>>`追加

git branch -avv
```
-a, --all               列出远程跟踪及本地分支
-v, --verbose           显示哈希值和主题，若参数出现两次则显示上游分支
-u, --set-upstream-to   <上游>改变上游信息
```
简单来说 upstream 就是于你本地分支对应的远端分支，push pull 或 fetch 时如果不指定远端分支，就会使用 upstream 分支。

> “origin” 并无特殊含义

远程仓库名字 “origin” 与分支名字 “master” 一样，在 Git 中并没有任何特别的含义一样。 
同时 “master” 是当你运行 git init 时默认的起始分支名字，原因仅仅是它的广泛使用， 
    “origin” 是当你运行 git clone 时默认的远程仓库名字。 
如果你运行 git clone -o booyah，那么你默认的远程分支名字将会是 booyah/master。

当 `git fetch` 命令从服务器上抓取本地没有的数据时，它并不会修改工作目录中的内容。 它只会获取数据然后让你自己合并。 
然而，有一个命令叫作 `git pull` 在大多数情况下它的含义是一个 `git fetch` 紧接着一个 `git merge` 命令。 

https://gogs.io/docs/installation
