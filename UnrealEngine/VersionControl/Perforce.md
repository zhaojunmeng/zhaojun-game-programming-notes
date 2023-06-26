# Perforce

[Using Perforce as Source Control](https://docs.unrealengine.com/5.2/en-US/using-perforce-as-source-control-for-unreal-engine/)

可以从上面的文章中，看到新建一个UE项目，需要将哪些文件加入到Perforce中。

另外上面文章讲了可以在Windows上面部署Perforce服务器。如果想要在自己Nas的Docker中部署Perforce服务器，可以参考这个仓库：[docker-sdp-perforce-server-for-unreal-engine](https://github.com/zhaojunmeng/docker-sdp-perforce-server-for-unreal-engine)

[Using P4IGNORE with P4V](https://portal.perforce.com/s/article/1282)
参考上面的文章，设置P4IGNORE

执行这个命令，然后重启P4V
p4 set P4IGNORE=.p4ignore

[p4ignore文件参考这个链接](https://gist.github.com/stungeye/28e116071c5a7052765d7752968ec56b)