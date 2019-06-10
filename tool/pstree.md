##### [进程查看 pstree :star:]($top) <b id="top"></b>
`查看Linux 进程结构`
`Linux pstree命令将所有行程以树状图显示，树状图将会以 pid (如果有指定) 或是以 init 这个
基本行程为根 (root)，如果有指定使用者 id，则树状图会只显示该使用者所拥有的行程。`

##### 例子 
`[root@iZn4pjam1xnbipZ ~]# pstree -a`

```node
systemd --switched-root --system --deserialize 22
  ├─AliYunDun
  │   └─18*[{AliYunDun}]
  ├─AliYunDunUpdate
  │   └─3*[{AliYunDunUpdate}]
  ├─agetty --noclear tty1 linux
  ├─agetty --keep-baud 115200 38400 9600 ttyS0 vt220
  ├─aliyun-service
  │   └─2*[{aliyun-service}]
  ├─atd -f
  ├─auditd
  │   └─{auditd}
  ├─chronyd
  ├─containerd
  │   └─8*[{containerd}]
  ├─crond -n
  ├─dbus-daemon --system --address=systemd: --nofork --nopidfile --systemd-activation
  ├─dhclient -1 -q -lf /var/lib/dhclient/dhclient--eth0.lease -pf /var/run/dhclient-eth0.pid -H AliYun eth0
  ├─dockerd -H fd:// --containerd=/run/containerd/containerd.sock
  │   └─8*[{dockerd}]
  ├─lvmetad -f
  ├─polkitd --no-debug
  │   └─6*[{polkitd}]
  ├─rsyslogd -n
  │   └─2*[{rsyslogd}]
  ├─sshd -D
  │   └─sshd    
  │       └─bash
  │           └─pstree -a
  ├─systemd-journal
  ├─systemd-logind
  ├─systemd-udevd
  └─tuned -Es /usr/sbin/tuned -l -P
      └─4*[{tuned}]

```

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
