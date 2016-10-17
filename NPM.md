# NPM的学习
	
	npm全局安装  npm install -g 安装在C:\Users\Administrator\AppData\Roaming\npm
	npm install 在当前目录node_modules下

	npm install --save  不需要手动的在package.json  dependencies下写模块和版本名  会自动添加到package.json dependencies下面

	npm install --save -dev 自动添加到  devDependencies下面


	npm init 则会初始化package.json文件



# node 知识点

	1. 事件循环

	2. 事件对象   EventEmitter 

	3. Buffer 对象

	4. stream 流  本质也是属于EventEmitter的子类
		1. data  有数据接收时触发
		2. end   接收完毕时触发
		3. finish 
		4. error  接收发生错误时触发
		
		readStream  读取流
		writeStream 输出流
		pipe        管道流  将一个流直接传入另外一个流  加速读取的速度

	5. 模块系统：

		1、关键字   
			exports 导出模块的接口
			module.exports  返回一个对象
			require  引入一个模块

		
	6.  
			__filename  返回文件的绝对路径
			
			__dirname   返回文件所在的目录
		