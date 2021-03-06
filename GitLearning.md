
[官方文档](https://git-scm.com/book/zh/v1/)



### 安装
```
sudo apt-get install git
```

### 配置
```
git config --list
git config --global user.name "user_name"
git config --global user.email "email_id"
```

### 初始化仓库
```
git init Mytest
cd Mytest
```
* 创建README
```
vim README
This is cyq' repo
```

> .gitignore不显示
> ls -al
> Ctrl+H


* GitHub中创建同名仓库
```
git remote add origin https://github.com/user_name/Mytest.git
```
* 推送主分支
```
git push origin master 
输入账号密码
```

### 克隆
```
git clone git+ssh://xxx@xxx/xxx.git
```
*clone报错没有私钥
```
ssh-keygen
Enter X3
cd ~/.ssh
cat id_rsa.pub   //拷贝到github
```

### 查看状态
```
git status
```

### 添加到stage
* 添加
```
git add xxx
git add .
```

* 撤销暂存
```
git reset .
git reset xxx
```
* 撤销修改
```
git checkout -- xxx
```

### 提交 
```
git commit -m "message"
git commit --amend -m 'commit by merge'   //合并提交
git commit -a -m 'commit directly'        //直接将工作区和暂存区的修改一起提交
```

### 查看当前项目清单
```
git ls-files 
```

### 删除
```
git rm xxx
git rm -r *
```

### 重命名
```
git mv file_from file_to
```

### 查看提交日志
```
git log
git log -n
git log --status   //查看变动情况
git log --stat
git log --pretty=oneline
git log --pretty=short
git log --pretty=full
git log --pretty=fuller
git log --pretty=format:"%h-%an,%ar:%s"
git log --pretty=format:"%h-%an,%ar:%s" --graph
git log --since =2.weeks
```
* 选项
```
-p
--world-diff
--stat
--shotstat
--name-only
--name-status
--abbrev-commit
--graph
--pretty
--oneline
--since="2008-10-01"
```

> 终端查看log如何退出
> ：q

### Diff
```
git diff
git diff --cached
git diff --staged
```

> git status 中文乱码
> git config core.quotepath off           //current repo
> git config --global core.quotepath off  //all repo

### Remote
```
git remote rename xxx yyy
git remote rm yyy

git remote -v
git remote ad [shortname][url]
git fetch origin
git pull
git push origin master
git remote show origin
```

### Tag
```
git tag
git tag -l 'v1.4.2' //查看特定大版本
git tag -a v1.4 -m 'my version 1.4'
git show v1.4
git tag v1.4l-lw  //轻量级标签
（git log --pretty=online）
git tag -a v0.5 9fceb02 -m 'add tag to exist commit'
git push origin v0.5
git push origin v0.5
git push origin --tags
```

### 检出
```
git checkout xxx
```


### 分支

























