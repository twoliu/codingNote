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