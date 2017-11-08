![directadmin_login_key_err](./image/directadmin_login_key_err.png)

问题：创建login key失败了，反馈信息：

执行失败，错误信息:Login Keys are disabled

解决办法：

	cd /usr/local/directadmin/data/users
	grep login_keys */user.conf
	grep 'login_keys=OFF' -nR */user.conf | awk -F: '{print $1}' | xargs -I {} sed -i 's/login_keys=OFF/login_keys=ON/g' {}
	/etc/init.d/directadmin restart

### 参考：

### [Connecting to DA with an API script, or giving out your DA password?](http://forum.directadmin.com/showthread.php?t=47667&p=249737#post249737)