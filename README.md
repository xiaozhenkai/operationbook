## 磁盘阵列
### 缓存策略
**Write-back:**
![Write-back with write-allocation](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c2/Write-back_with_write-allocation.svg/1000px-Write-back_with_write-allocation.svg.png)

**Write-through:**
![Write-through with no-write-allocation](https://upload.wikimedia.org/wikipedia/commons/thumb/0/04/Write-through_with_no-write-allocation.svg/2000px-Write-through_with_no-write-allocation.svg.png)


阅读：
#### [raid 控制器对系统性能的影响](https://highdb.com/raid-%E6%8E%A7%E5%88%B6%E5%99%A8%E5%AF%B9%E7%B3%BB%E7%BB%9F%E6%80%A7%E8%83%BD%E7%9A%84%E5%BD%B1%E5%93%8D/)

#### [Write-through, write-around, write-back: cache explained](http://www.computerweekly.com/feature/Write-through-write-around-write-back-Cache-explained)

#### [阵列Cache写机制：Write-through与Write-back区别](http://dangzhiqiang.blog.51cto.com/7961271/1402145)

**扩展阅读：**
​	
[NVDIMM](https://en.wikipedia.org/wiki/NVDIMM) **non-volatile dual in-line memory module 非易失性双列直插式内存模块**
​	
[关于按字寻址和按字节寻址的理解](http://blog.csdn.net/lishuhuakai/article/details/8934540)

[Cache 的 write back 和 write through](http://benjr.tw/20361)

## 分布式存储
### Ceph
#### 增减OSD：
[**替换OSD操作的优化与分析**](http://www.zphj1987.com/2016/09/19/%E6%9B%BF%E6%8D%A2OSD%E6%93%8D%E4%BD%9C%E7%9A%84%E4%BC%98%E5%8C%96%E4%B8%8E%E5%88%86%E6%9E%90/)

[‘**noout’ flag in Ceph**](https://arvimal.blog/2015/05/28/what-does-the-noout-status-on-the-osds-actually-do/)
```
ssd cache 日志 journal
mon/osd 1 2 3 4 5 五台机器当存储，用户存储的时候访问mon，mon在告诉用户去哪里存储数据
ceph 监控 ceph-dash
```
硬盘测试

Reliable Autonomic Distributed Object Store （RADOS）可靠的自主分布式对象存储 bench
​	
### MooseFS
#### [分布式文件系统之MooseFS----介绍](http://nolinux.blog.51cto.com/4824967/1600890)
#### [分布式文件系统之MooseFS----部署](http://nolinux.blog.51cto.com/4824967/1601385)
#### [分布式文件系统之MooseFS----管理优化](http://nolinux.blog.51cto.com/4824967/1602616)
#### [MFS学习总结](http://www.cnblogs.com/oubo/archive/2012/05/04/2482893.html)
```
	存储模式？goal（副本数）
	单点故障？（扩展：Ceph 多元数据服务器）
```
[MooseFS和Hadoop两个分布式文件系统各有什么优缺点？](https://zhihu.com/question/22171041/answer/20521040) 

[扩展：分布式文件系统MFS、Ceph、GlusterFS、Lustre的比较](http://blog.csdn.net/dipolar/article/details/50154349)

[扩展：ceph存储 FUSE原理总结](http://blog.csdn.net/skdkjzz/article/details/42299751)
​	
### cloudboot
#### [KICKSTART无人值守安装](http://www.zyops.com/autoinstall-kickstart)

## database
### RDBMS
#### MySQL
##### 读写分离
###### MyCAT
[Mysql中间件】Mycat安装部署+读写分离](https://segmentfault.com/a/1190000009520414)
​	
##### ATLAS(单点问题？)
[通过Atlas实现MySQL读写分离](https://my.oschina.net/sunhaojava/blog/907430)

[MySQL + Atlas --- 部署读写分离](http://www.cnblogs.com/yyhh/p/5084844.html#l01)

[使用Atlas配置MySQL读写分离](http://www.361way.com/atlas-mysql/5310.html)

[mysql中间件研究（Atlas，cobar，TDDL）](http://www.guokr.com/blog/475765/)

##### MySQL性能监控
[MySQL 性能监控4大指标——第一部分](http://blog.oneapm.com/apm-tech/754.html)
​		
[**扩展阅读**：Mysql配置参数sync_binlog说明](http://www.cnblogs.com/Cherie/p/3309503.html) [参考2](https://my.oschina.net/u/1433006/blog/1088697)
​	

### NoSQL
#### MongoDB
[【分享】Mongodb线上真实事故案例](https://cnodejs.org/topic/55c97a997a5d91fa63fe9ce7)

[Mongodb 实战优化  ](http://snoopyxdy.blog.163.com/blog/static/6011744020157511536993/)



## tc

### [使用 linux 下的 TC 进行服务器流量控制](http://www.php-oa.com/2009/06/23/linux_tc.html)

### [Linux 高级流控](https://www.ibm.com/developerworks/cn/linux/1412_xiehy_tc/index.html)

### [Linux 网络堆栈的排队机制](http://blog.jobbole.com/62917/)

### [Advanced traffic control](https://wiki.archlinux.org/index.php/Advanced_traffic_control#Hierarchical_Token_Bucket_.28HTB.29)

### [Differentiated Service on Linux HOWTO](http://web.opalsoft.net/qos/default.php?p=linux101-ds)

### [浅谈RAID写惩罚（Write Penalty）与IOPS计算](https://community.emc.com/docs/DOC-26624)

### [raid 控制器对系统性能的影响](https://highdb.com/raid-%E6%8E%A7%E5%88%B6%E5%99%A8%E5%AF%B9%E7%B3%BB%E7%BB%9F%E6%80%A7%E8%83%BD%E7%9A%84%E5%BD%B1%E5%93%8D/)

### [MySQL高可用架构之MHA](http://www.cnblogs.com/gomysql/p/3675429.html)

## MTU/IP/TCP

### [【大咖讲网络】MTU导致的悲剧](http://www.sohu.com/a/158388912_262201)

### [网络03：网络连通性测试的相关命令](http://higoge.github.io/2017/02/01/net03/)

### [MTU参数对运营商网络的影响及配置建议](http://www.h3c.com/cn/d_201502/853983_97665_0.htm)

### [Understand MTU and MRU – The Full Story](http://www.networkers-online.com/blog/2016/03/understand-mtu-and-mru-the-full-story/)

### [MTU and ping size confusion](http://www.networkers-online.com/blog/2010/02/mtu-and-ping-size-confusion/)

### [网络虚拟化中的 offload 技术：LSO/LRO、GSO/GRO、TSO/UFO、VXLAN](http://blog.csdn.net/yeasy/article/details/19204639/)

### [IP头，TCP头，UDP头，MAC帧头定义](http://www.cnblogs.com/li-hao/archive/2011/12/07/2279912.html)

### [理解 Linux 网络栈（2）：非虚拟化Linux 环境中的 Segmentation Offloading 技术](http://www.cnblogs.com/sammyliu/p/5227121.html)

[]()
[]()
[]()
[]()