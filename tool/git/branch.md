##### [远程分支交互](#top) <b id="top"></b>
----

##### 1.查看远端服务器所拥有的分支
```powershell
git branch -r
```

##### 2.推送本地分支到远程仓库
`把创建的本地dev1推送到远程仓库：`
```powershell
git push --set-upstream origin 分支名
```

##### 3.远程git仓库里的指定分支拉取到本地（本地不存在的分支） 
```powershell
git checkout -b 本地分支名 origin/远程分支名
```

##### 4.拉取失败的话可能 需要重新拉取一下

```node
git fetch
```
