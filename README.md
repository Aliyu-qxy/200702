### 初学git

1 初始化git库

```shell
git init
```

2  换行符差异

```shell
deepin=乌班图（全局）
git config --global core.autocrlf input
contos
git config --global core.autocrlf true
```

3  配置个人名称和邮箱和登录无关

```shell
当前目录.git可查看
git config user.name aly
git config user.email 1027580018@qq.com
```

   3.全局名称邮箱配置

```shell
家目录.gitconfig可查看
git config --global user.name aly
git config --global user.email 1027580018@qq.com
```

4 查看暂存区状态

```shell
git status  查看提交状态


kgc@kgc-1022:~/workspace/200701$ git status
位于分支 master

尚无提交

未跟踪的文件:
  （使用 "git add <文件>..." 以包含要提交的内容）

	haha.txt

提交为空，但是存在尚未跟踪的文件（使用 "git add" 建立跟踪）
```

5 将文件添加到索引（暂存区）

```shell
git add 文件名
检查状态

kgc@kgc-1022:~/workspace/200701$ git status
位于分支 master

尚无提交

要提交的变更：
  （使用 "git rm --cached <文件>..." 以取消暂存）

	新文件：   haha.txt

```

​       5.5将文件从暂存区删除

```
git rm --cached 文件名
```

6  提交到本地库

```
-m 日志  日志描述
git commit -m "200701第一个提交文件" 文件名
```

7 文件修改后提交本地库

```
修改文件
git add
git commit -m "修改的haha.txt"（不需要写名字）
```

8 查看每次提交的log日志

```
git log

美观看法
git log --pretty=oneline
简化美观看法
git log --oneline
git reflog

```

9 本地库版本控制（删除亦可恢复）

```

hard可以回到任意版本  最后跟类似uuid码（简单版即可）
git reset --hard 17e2769
```

![image-20200702022607699](git指令笔记.assets/image-20200702022607699.png)

## github远程托管

1 --新建一个仓库

​		选择协议，选择格式

2  --跟随提示动作

​	  1 创建仓库

​		

```shell
echo "# 200702" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/Aliyu-qxy/200702.git
git push -u origin master
```

