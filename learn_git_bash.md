# 1.常用命令行

```
$ cd + 文件路径
/*cd (change directory):转换到某文件位置；*/
```

```
$ makdir + 文件名
/*mkdir(make directory):创建目录*/
```

```
$ pwd 
/*pwd(print working directory):打印当前目录位置*/
```

```
$ git init
/*初始化仓库(注意，得在创建的目录下初始化才能将创建的目录转化为仓库)*/
```

```
$ git status
/*查看当前仓库状态*/
```

```
$ git add + 文件名
/*将文件添加到暂存区(注意，该文件必须在当前目录下面)*/
```

```
$ git commit -m + 描述文字
/*将文件提交到仓库*/
```

```
$ git diff + 文件名
/*diff(diffence):查看具体更改内容*/
```

```
$ git log (--pretty=oneline)
/*产看日志(加上括号里面的为每个日志显示为一行)*/
```

```
$ git reset --hard commit_id
/*作用：回滚到某个历史工作区
注解：
1.commit_id指的是某个commit的ID；
2.此时再用git log查看日志，就没有在回退时间之后的了。若要查看之后的，可以用git reflog*/
```

```
$ git reflog
/*reflog(reference log)查看所有更新分支的命令和引用*/
```

```
$ cat + file_name
$ cat  file1 file2 > target_file
/*cat(print and concatenate)
1.打印文件
2.合并文件*/
```

```
$ git checkout -- <file_name>
/*将未存入暂存区的修改撤销，即让这个文件回到最近一次git commit或git add时的状态*/
$ git reset HEAD <file_name>
/*将存入暂存区的修改回退到工作区*/
```



# 2. Git工作原理

1.各历史工作区都有一个指针HEAD指向它

![](pictures/learn_git_bash/1.png)

2.工作区和暂存区

在创建版本库的时候，Git会自动帮我们创建一个master分支，master分支存储着我们的历史文件。

![](pictures/learn_git_bash/2.jpg)

我们先用add把修改添加到暂存区(stage)，再用commit把修改一次性添加到master分支，这时如果没有其他操作，我们的工作区就“干净”了。

注意：Git和其他管理系统不一样的是，它是存储的修改，而不是文件。所以我们每修改一次，就得把修改add入stage。
