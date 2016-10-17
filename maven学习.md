## Maven学习
	
	mvn compile  编译类文件  到  target classes里面
	mvn test     测试   
	mvn clean    清除target 
	mvn package  打包【】
	mvn install  将打包好的jar包安装到本地的maven仓库中


### maven包的依赖范围
	
	test  仅在测试范围有效  测试包[***这个不会有maven的依赖传递***]
	provider  编译和测试时依赖 打包的时候不依赖  servlet-api[运行的服务器里面提供]
	runtime   编译时不依赖 测试和打包的时候都依赖  数据库驱动包
	compiler  编译和打包的时候都依赖
	
	A 项目依赖 log4j  1.1.9
	B 项目依赖 log4j  1.2.1
	C 依赖项目A,B     依赖级别相同,则取先依赖的那一个 
					 依赖级别不同,则取依赖级别最短的一个

	<exclusions>
		<exclusion></exclusion>  排除依赖[产生包冲突的时候使用]
	</exclusions>


### maven的继承和聚合
	继承 统一管理 各个模块的工程

### maven的私服安装 nexus

### maven的插件
	
	 
	
	
	
	
	
	
	
	
	



 
	
	
	