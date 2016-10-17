# linux常用命令总结

	* 查看端口号是否被占用     netstat -tln | grep 端口号 (只能看端口的使用情况)

	* 查看端口使用的详情    lsof -i :端口号    (具体是指的哪个应用占用)

	* 杀掉进程   kill -9 pid ----后面紧跟进程pid
	
	* ifconfig 查看本机ip   【ifconfig|grep 'Bcast'】

	* su  切换用户
	
	* ls  列出文件目录
	
	* pwd列出当前目录

	* rmdir删除空的文件   rm删除非空文件

	* cp -a source target   常用命令，复制  -i 复制有重复会提示是否覆盖

	* mv -f强制移动(直接覆盖)  -i询问                                   移动文件

	* cat 从第一行查看文件
	* tac 从最后一行输出
	* nl  从第一行输出并显示行号


	* vi 命令
		* vi filename 一般模式 文件不存在则创建
		* 按下  i     静茹编辑模式
		* ： 退出编辑模式 
			* 后面加载wq 保存退出
			*  w保存
			*  q! 不保存退出


	* yum 软件包管理器










	
	* tar 命令
		* tar -cf xx.tar file   将file打包到xx.tar文件中
		* tar -tf xx.tar        列出xx.tar中的文件列表
		* tar -xf xx.tar        解压出xx.tar里面的文件


>>http://jingyan.baidu.com/album/20b68a885a3607796cec622c.html   V6.5使用中文输入法方法


# shell 脚本
	
	#!/bin/bash
	your_name = 'yunux'
	echo ${your_name}
	echo "Hello Yunux!"
	string="runoob is a great company"
	echo `expr index "$string" r`  查找r在字符串中的位置
	echo ${string:1:4} #从第二个开始取，取四个长度
	echo ${#string}   #取长度
	
	array_name=(value0 value1 value2 value3)
	echo ${#array_name[*]}  #length
	echo ${array_name[@]}  #value 

> 执行脚本的时候需要赋予脚本权限  chmod +x ./===  脚本路径
> 在使用变量的时候采用$ 符号
> 
	
	
	
