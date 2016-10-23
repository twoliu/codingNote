### java nio
> 提前理好几个概念
	同步  异步 阻塞 非阻塞
	1. 同步  : 程序在一个代码一直执行,直到执行完毕返回值,才能继续执行后面的操作
	2. 异步  : 程序执行一行代码,不用等待结果返回,会交给内核去操作
	3. 阻塞  : 一直执行直到执行完毕有返回结果,导致线程在这里挂起   
	4. 非阻塞:程序执行立即返回结果,结果不对在发送请求,直到请求正确为止 利用多线程来理解阻塞和非阻塞
>




> nio ->new io 是基于channel(通道)和buffer(缓冲区) 来操作数据的
	
	1. 缓冲区

		flip()   是缓冲区开始变为读模式(位置切换到0开始读)
		clear()  清空缓冲区
		
		三个特性 ： capacity  缓冲区的容量
				   limit    写模式:等于capacity 读模式:为写模式的position值
				 position   当前读到的位置 读模式:切换为0  写模式 表示为当前位置


	2. 通道  文件io File IO  流io stream IO
		1. FileChannel 不能直接创建 且永远是阻塞的  不能与selector一起使用
		2. SocketChannel
		3. ServerSocketChannel
		4. DatagramChannel
	
	3. 异步io
	4. Selectors(选择器) 
		open 打开选择器
		selector  获取选择到的事件,有连接进来返回值，没有则返回0
		selectorkeys



