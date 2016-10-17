# Spring整合Quartz 执行定时任务

## 基本的任务调度
	1. quartz的jar包
	2. Spring-context-support.jar的支持
	> 注意版本的整合  2.x以上的quartz需要spring3.1以上的版本支持

	方式一:
		自定义任务bean类
		`public class TestTask  {

   			 protected static final Logger log = Logger.getLogger(TestTask.class);

    		public void doIt() {
        log.info("------定时器任务执行-------");
        	System.out.println("==============执行			================");
    		}

		}`

		配置bean
			
		配置任务管理器  
		<bean id="jobDetail" class="org.springframework.scheduling.quartz.MethodInvokingJobDetailFactoryBean">
        <property name="targetObject"   ref="testTask"/>
        <property name="targetMethod"   value="doIt"/>
        <property name="concurrent"     value="false"/>
    	</bean>	
		
		配置任务调度器
		<bean id="cronTrigger" class="org.springframework.scheduling.quartz.CronTriggerFactoryBean">
        <property name="jobDetail"  ref="jobDetail"/>
        <!--每隔两秒钟开始执行-->
        <property name="cronExpression" value="0/2 * * * * ?"/>
    	</bean>

		配置总的任务调度器
		<bean class="org.springframework.scheduling.quartz.SchedulerFactoryBean">
        <property name="triggers">
            <list>
                <ref bean="cronTrigger"/>
            </list>
        </property>
    	</bean>

	方式二：
		
		自定义class继承Job类
		重写excute方法
		配置Jobdetail
		<bean name="exampleJob" class="org.springframework.scheduling.quartz.JobDetailBean">
		<property name="jobClass" value="com.spring.task.TaskOne" />
		<property name="jobDataAsMap">
			<map>
				<entry key="timeout" value="5" />
			</map>
		</property>
		</bean>	


## 动态的创建 修改 删除 添加定时任务 见
	
> http://snailxr.iteye.com/blog/2076903?page=2#comments