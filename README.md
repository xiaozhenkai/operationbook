# 基础篇
## 存储
### 磁盘阵列
#### 缓存
	Write-back
![Write-back with write-allocation](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c2/Write-back_with_write-allocation.svg/640px-Write-back_with_write-allocation.svg.png)

	Write-through
![Write-through with no-write-allocation](https://upload.wikimedia.org/wikipedia/commons/thumb/0/04/Write-through_with_no-write-allocation.svg/2000px-Write-through_with_no-write-allocation.svg.png)
	Write-around
reference：
	http://www.computerweekly.com/feature/Write-through-write-around-write-back-Cache-explained
	
	扩展阅读：
	
	https://en.wikipedia.org/wiki/NVDIMM
	
	http://blog.csdn.net/lishuhuakai/article/details/8934540
	
Ceph
	增加OSD：
		[替换OSD操作的优化与分析](http://www.zphj1987.com/2016/09/19/%E6%9B%BF%E6%8D%A2OSD%E6%93%8D%E4%BD%9C%E7%9A%84%E4%BC%98%E5%8C%96%E4%B8%8E%E5%88%86%E6%9E%90/)
		[‘noout’ flag in Ceph](https://arvimal.blog/2015/05/28/what-does-the-noout-status-on-the-osds-actually-do/)
	ssd cache 日志 journal
	mon/osd 1 2 3 4 5 五台机器当存储，用户存储的时候访问mon，mon在告诉用户去哪里存储数据
	ceph 监控 ceph-dash
	
	硬盘测试
	Reliable Autonomic Distributed Object Store （RADOS）可靠的自主分布式对象存储 bench
	
MooseFS
	[分布式文件系统之MooseFS----介绍](http://nolinux.blog.51cto.com/4824967/1600890)
	[分布式文件系统之MooseFS----部署](http://nolinux.blog.51cto.com/4824967/1601385)
	[分布式文件系统之MooseFS----管理优化](http://nolinux.blog.51cto.com/4824967/1602616)
	[MFS学习总结](http://www.cnblogs.com/oubo/archive/2012/05/04/2482893.html)
	存储模式？goal（副本数）
	单点故障？（扩展：Ceph 多元数据服务器）
	
	MooseFS和Hadoop两个分布式文件系统各有什么优缺点？ - 回答作者: 严林 https://zhihu.com/question/22171041/answer/20521040 (想看更多？下载 @知乎 App：http://weibo.com/p/100404711598 )
	[扩展：分布式文件系统MFS、Ceph、GlusterFS、Lustre的比较](http://blog.csdn.net/dipolar/article/details/50154349)
	[扩展：ceph存储 FUSE原理总结](http://blog.csdn.net/skdkjzz/article/details/42299751)
	
cloudboot
	[KICKSTART无人值守安装](http://www.zyops.com/autoinstall-kickstart)
	
读写分离
	MyCAT
		[Mysql中间件】Mycat安装部署+读写分离](https://segmentfault.com/a/1190000009520414)
	
	ATLAS(单点问题？)
		[通过Atlas实现MySQL读写分离](https://my.oschina.net/sunhaojava/blog/907430)
		[MySQL + Atlas --- 部署读写分离](http://www.cnblogs.com/yyhh/p/5084844.html#l01)
		[**使用Atlas配置MySQL读写分离**](http://www.361way.com/atlas-mysql/5310.html)
		[mysql中间件研究（Atlas，cobar，TDDL）](http://www.guokr.com/blog/475765/)
	MySQL性能监控
		[MySQL 性能监控4大指标——第一部分](http://blog.oneapm.com/apm-tech/754.html)
		
		[**扩展阅读**：Mysql配置参数sync_binlog说明](http://www.cnblogs.com/Cherie/p/3309503.html) [参考2](https://my.oschina.net/u/1433006/blog/1088697)
	

NoSQL
	MongoDB
		[【分享】Mongodb线上真实事故案例](https://cnodejs.org/topic/55c97a997a5d91fa63fe9ce7)
		[Mongodb 实战优化  ](http://snoopyxdy.blog.163.com/blog/static/6011744020157511536993/)
