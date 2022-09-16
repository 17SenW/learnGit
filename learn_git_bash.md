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
$ git reset --hard HEAD^
/*作用：回滚到某个历史工作区
注解：
1.HEAD指的是当前commit的ID；
2.一个^表示往回退1个，多个可以用"~数字"
3.此时再用git log查看日志，就没有在回退时间之后的了。若要查看之后的，可以用git reflog*/
```

```
$ git reflog
/*查看所有命令*/
```

