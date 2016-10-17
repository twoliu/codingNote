# java异常
	1. Throwable
		1. error    硬伤无法改变
		2. exception  
			1. RuntimeException 运行时异常  系统会自动抛出  程序本身有问题
			2. 检查异常 
				1. IOException  需要手动的捕获处理


	2. 处理异常
		1. try-catch 
		       	后面接多重catch语句块  catch 捕获的异常先子类在父类
				
				
				
		2. try-catch-finally   finally块里面的语句始终会执行



	3. 抛出异常
		1. throw 抛出一个异常  用于方法体内

		2. throws 声明这个类会抛出异常 用于方法上


	4. java异常链


# java的可变参数 
	形式   ...args  jvm会隐式的创建一个args[] 数组传参  而且必须放在最后


# java泛型的见解
参考下文的连接 [java泛型擦除](http://www.hollischuang.com/archives/226 "java泛型擦除")

>虚拟机中没有泛型，只有普通类和普通方法,所有泛型类的类型参数在编译时都会被擦除,泛型类并没有自己独有的Class类对象。比如并不存在List<String>.class或是List<Integer>.class，而只有List.class。 2.创建泛型对象时请指明类型，让编译器尽早的做参数检查