##### [进程查看 pstree :star:]($top) <b id="top"></b>
`查看Linux 进程结构`
`Linux pstree命令将所有行程以树状图显示，树状图将会以 pid (如果有指定) 或是以 init 这个
基本行程为根 (root)，如果有指定使用者 id，则树状图会只显示该使用者所拥有的行程。`


##### :one: [语法](#top)
```shell
pstree [-a] [-c] [-h|-Hpid] [-l] [-n] [-p] [-u] [-G|-U] [pid|user]

pstree -V 版本查看
```

```node
-a，—arguments显示命令行参数
-A，--ascii使用ascii绘制行字符
-c, --compact 不压缩相同子树
-h，--highlight-all 突出显示当前进程及其祖先进程
-g，-show pgis 显示进程组ID；表示-C
-G，--VT100 使用VT100线条绘制字符
-l，--长不截断长线
-n，-numeric sort按pid排序输出

-N type，--ns sort=按名称空间类型（ipc、mnt、net、pid、user、uts）进行类型排序
-p，-show pids显示pids；暗示-c
-s，--显示父进程显示所选进程的父进程
-S，-ns更改显示命名空间转换
-u，-uid更改显示uid转换
-U，-unicode使用utf-8（unicode）线条绘制字符
```

##### :two: [常用命令](#top)
```node
# pstree -a  //查看进程树 包括子进程关系

# pstree -g  //查看进程树 包含进程 id 包含子进程 并且展开子进程

# pstree -apnh //显示进程间的关系

# pstree -u //显示用户名称

# pstree -aug //显示......
```
