### java nio
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



