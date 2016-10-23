# Spring  模糊点
	注解 
	1. @Autowired  默认通过类型配置
	2. @Resource    默认通过属性名来配置
	3. @RestController  相当于@Controller 和 @ResponseBody
	4. @Exceptionhandle  处理局部异常
	5. 在@ControllerAdvice 里面添加Exceptionhandle 代表全局异常 

	切面aop注解
	1. @Aspect 指定切面
	2. @Order 指定切面的优先级
	3. @before @after @afterreturnning @Arround 通知的方式
	4. @Pointcut 切点

	Spring事务的管理
	1. 基于注解的事务
		1. @Transonctional
			1. propagation  指定事务的传播行为属性
			2. isolation        指定事务的隔离级别
			3. readonly      是否为只读事务
			4. timeout       指定事务强制回滚超时
	
	2. 基于xml配置 (利用aop思想)



###事务的隔离级别
	
	脏读
	不可重复读
	虚读