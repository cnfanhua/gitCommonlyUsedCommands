### git 全局设置

```c
git config --global user.name "yyyy"
git config --global user.email "xxx@xxx.com"
```

### ssh-keygen

```c
ssh $ ssh-keygen -t rsa -C "youremail@example.com"
```

### clone 仓库

```c
git clone git@github.com/xx/xx.git
```

### 初始化仓库

```c
git init
```

### 关联到远程仓库

```c
git remote add origin git@github.com/xx/mxx.git
```

### 拉取远程仓库内容

```c
git pull origin master
```

### 添加文件到 Git 仓库

```
1 git add <file> // 可以反复使用，添加多个文件
1 git add .  // 添加全部(排除.gitignore中的文件)

2 git commit -m '注释'
```

### 推送到远程仓库

```c
git push origin master
```

### 查看工作区状态

```c
git status
```

### 查看提交历史

```c
git log
```

### 返回到某个节点

```c
git reset --hard HASH  //返回到某个节点，不保留修改。
git reset --soft HASH  //返回到某个节点。保留修改
```

### 分支相关

```c
git branch //查看本地分支
git branch -a //查看远程分支

git branch <name>  //创建分支
git checkout <name>  //切换分支

git merge dev  //合并dev分支到当前分支

git branch -d <name>  //删除本地分支
git push origin --delete <name>  //删除服务器分支
```

### 删除 Git 上的远程文件/文件夹

```c
git rm -r --cached test    // 单个文件
git rm -r --cached .       // 全部

git add .
git commit
git push origin master
```
