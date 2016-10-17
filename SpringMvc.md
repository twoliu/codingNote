# Spring Mvc 

	属于Spring的一个模块
	
	* 配置springmvc的配置文件模块就是配置一个servlet 【一个siapatchServlet中央调度器】

	* 理解springMVC的整个请求流程 【映射处理器,处理适配器,视图解析器】
		*配置适配器和处理器映射器的时候可以使用mvc注解驱动代替
		*适配器配置可以配置一些自定义的参数转换器

	* Spring的参数绑定:
		* 属性名与传递的参数一致，就能进行参数绑定
		* 如果参数传递的是对象 则前端传递的参数名（name)与对象的属性名一致就能完成绑定




## SpringMVC 上传图片 
	
	* 上传图片依赖 conmmons-upload commons-io 两个包
	* 配置上传图片解析器bean到配置文件


## SpringMVC   json数据的交互
	
	* @RequestBody   请求数据封装为json格式
		$.ajax({
		url : ,
		contentType : 'application/json,charactType="utf-8"',
		data : 'key=value&key=value'
	}) 

	* @ResponseBody  将返回的结果封装为Json格式返回


## SpringMVC 的validation  校验器 


## SpringMVC 的异常处理  配置统一的异常处理器
	
	** 要求controller service dao 有异常全部向上抛出
	* 在处理器适配器中配置异常处理


## SpringMVC 的restfull
	1. 配置dispacherServlet 的拦截为  /  静态资源的访问 需要用 <mvc:resource location mapping>  另外配置
	2. 使用@Pathvariable 将传递的参数跟形参绑定
	

## SpringMVC 的拦截器
	
	拦截器是通过处理器映射器发起返回的
	在<mvc:intecepter> 中配置拦截器类 可以配置多个 
	/** 拦截所有层的处理
	/*  只能拦截一层的处理
	
	
	
	
	
		
	
	
	





