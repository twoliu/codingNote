# sprring 和 mybatis 的整合
> 整合的两种思路

	1. spring通过mapper来整合
		1. 不用在写实现类，通过spring生成的代理对象来执行方法


	2. spring通过原始的dao和daoImpl来整合
		1. 写实现类在实现类里面调用mapp.xml的方法


* 整合必须的包
> sqlMapConfig.xml   配置一些mybatis的基本参数
	
	设置常量,加载mapper.xml资源 ,定义po类的扫描包


> Spring 

	管理datasource 
	加载sqlMapConfig.xml的配置环境
	定义扫描器 ： MapScannerFactory 工厂
	 用于生成代理对象
	





