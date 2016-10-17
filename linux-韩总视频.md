# linux 加强
	
	命令 
	shutdown -h now 关机
	shutdown -r now 重启
	reboot   重启
	pwd      显示当前目录


	useradd XXX  添加用户
	passwd    修改密码
	userdel XXX  删除用户
	userdel -r XXX 删除用户以及所有文件信息
	exit   注销当前用户
	
	ls    列出文件
	ls -a 显示隐藏文件
	ls -l 显示长列表格式

	mkdir  创建目录
	mkdir -p 创建多级目录
	rmdir  删除空的文件夹
	cp  复制
	rm  删除文件
	
	|   这就是管道命令 把上一个命令的结果交给这个管道后面的命令
	grep  查找关键字
	find / -name XXX 在根目录开始查找名为XXX的文件
	
	> 覆盖写
	>>  续写

		
		
		
		
	基本的vi编辑器
	vi  文件名（不存在则创建）
	i   进入编辑模式
	esc 退出编辑模式
	:   命令模式
	wq  保存退出

	linux的文件目录
	root   root用户相关文件
	home   存放普通用户的文件
	etc    存放配置文件
	usr    软件的默认安装位置
	mnt    挂载目录
	bin    基本的命令
	sbin   需要权限的命令
	var    经常变动的文件


	linux 用户管理
	
	/etc/inittab/   更改计算机的启动级别 有7种状态
	/etc/group      查看计算机的用户组  
	/etc/passwd     查看所有用户列表
	groupadd 添加组
	useradd -g 组名 用户  将用户添加到某个组
	ls -l 查看文件信息
	-rw-r--r--. 1 root root 228 Sep 24 07:21 1.txt
	- 代表普通文件
	d 代表的是目录
	l 代表链接文件
	rw 该文件用户拥有 r 读(用4表示) w写(用2表示) x可执行(1)
	-r  该用户所在组对该文件的权限
	--r 其它用户对该文件的权限

	chmod 770 XXX 修改该文件的读写权限给所在组的所有人(7=4+2+1) 

	usermod -g 组名 用户  修改用户所在的组

	
	mount /mnt/cdrom  挂载文件到linux这个目录下
	umonnt /mnt/cdrom  卸载
	
	linux 分区
	>>>windows 主分区和扩展分区 相加不能超过四个  
	主分区
	
	扩展分区 : 不能直接使用 需要分成逻辑分区  逻辑分区数量没有限制
	
	fdisk -l   查看分区 
	df 目录     查看目录挂载在哪个分区
	df -l      查看磁盘的使用情况

	linux  shell 脚本

	tcp/ip协议
	应用层 smtp ftp http
	传输层 解析数据
	网络层 定位地址 确定链路 
	链路层 与硬件驱动对话
	
	修改ip /etc/sysconfig/network-scripts/ifcfg-eth0
	/etc/rc.d/init.d/network restart 网络配置生效

	yum rpm 包管理器   yum比rpm更方便
	
	
	
	linux任务调度命令
	crontab -e 写任务调度程序
	
	*    *     *    *   *
 	分钟  小时  月   年   星期几


	crontab -r 终止任务
	crontab -l 列出当前的任务

	linux 查看进程
	
	ps -aux   静态的查看
	
	top 动态的查看

	复制
	cp -rf src des 复制文件夹 
	cp src des    复制文件