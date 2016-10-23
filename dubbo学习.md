### Zookeeper 学习
	集群管理,统一服务命名,分布式的消息,锁,监控集群
	单点配置
	集群配置

### dubbo-admin 管理界面安装,指向zookeeper

### Spring 高版本与dubbo的整合
	<dependency>
      <groupId>com.alibaba</groupId>
      <artifactId>dubbo</artifactId>
      <version>2.5.3</version>
	<!--去掉内置的Spring支持-->
      <exclusions>
      	<exclusion>
      		<artifactId>spring</artifactId>
      		<groupId>org.springframework</groupId>
      	</exclusion>
      </exclusions>
    </dependency>
    <dependency>
      <groupId>org.apache.zookeeper</groupId>
      <artifactId>zookeeper</artifactId>
      <version>3.4.8</version>
      <!--更改log4j的支持-->
      <exclusions>
        <exclusion>
           <groupId>log4j</groupId>
           <artifactId>log4j</artifactId>
        </exclusion>
      </exclusions>
    </dependency>
    <dependency>
      <groupId>log4j</groupId>
      <artifactId>log4j</artifactId>
      <version>1.2.16</version>
    </dependency>
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
		

	
	