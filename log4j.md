# log4j 使用
	
	1. 下载log4j的jar 包
	2. 配置log4j.properties 配置文件
	3. 获取日志记录器
		1. private Logger log = Logger.getLogger(clazz)
		2. 在需要记录日志信息的代码处加入log.info("")
			1. log.info("")
			2. log.error("")
			3. log.debug("")
			4. log.warn("")


> 注意log4j的配置文件写法
	
	> 配置日志记录的级别  
	【日志级别的高低 四个等级 error warn info debug等级从高到底 如果当前的级别为info，则debug级别的日志不会记录】
	> [stdout D E 指定输出的目录]
	log4j.rootLogger = debug,stdout,D,E
	
	#log4j.appender.stdout = org.apache.log4j.ConsoleAppender
	log4j.appender.stdout = org.apache.log4j.FileAppender
	log4j.appender.stdout.File = E://logs/Alllog.log
	log4j.appender.stdout.Append = true
	#log4j.appender.stdout.Target = System.out
	log4j.appender.stdout.layout = org.apache.log4j.PatternLayout
	log4j.appender.stdout.layout.ConversionPattern = [%-5p] %d{yyyy-MM-dd HH:mm:ss,SSS} method:%l%n%m%n
	
	
	log4j.appender.D = org.apache.log4j.DailyRollingFileAppender   #指定每天生成日志
	log4j.appender.D.File = E://logs/log.log                       #指定日志生成的文件夹
	log4j.appender.D.Append = true                                 #指定是否在当前文件后面自动追加日志
	log4j.appender.D.Threshold = DEBUG                             #指定日志的级别
	log4j.appender.D.layout = org.apache.log4j.PatternLayout       #自定义日志的格式
	log4j.appender.D.layout.ConversionPattern = %-d{yyyy-MM-dd HH:mm:ss} [ %t:%r ] - [ %p ] %m%n
	
	
	log4j.appender.E = org.apache.log4j.DailyRollingFileAppender
	log4j.appender.E.File = E://logs/.error.log
	log4j.appender.E.Append = true
	log4j.appender.E.Threshold = ERROR
	log4j.appender.E.layout = org.apache.log4j.PatternLayout
	log4j.appender.E.layout.ConversionPattern = %-d{yyyy-MM-dd HH:mm:ss} [ %t:%r ] -[ %p ] %m%n



> Spring 整合log4j日志框架

	<!-- 设置根目录 -->  
    <context-param>    
        <param-name>webAppRootKey</param-name>    
        <param-value>webapp.root</param-value>    
    </context-param>    

    <context-param>  
        <param-name>log4jConfigLocation</param-name>  
        <param-value>/WEB-INF/classes/log4j.properties</param-value>  
    </context-param>  
    <!-- 3000表示 开一条watchdog线程每60秒扫描一下配置文件的变化;这样便于日志存放位置的改变 -->  
    <context-param>    
         <param-name>log4jRefreshInterval</param-name>    
         <param-value>3000</param-value>    
    </context-param>   
    <listener>  
        <listener-class>org.springframework.web.util.Log4jConfigListener</listener-class>  
    </listener>


> 与slf4j整合