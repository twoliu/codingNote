### java conCurrent 包解析
	
	conCurrentHashMap  分片存储 segment 




### ArrayList 源码解析
	
	号外 : transient  修饰的变量不会被序列化

	每次添加元素都会增加数组的容量,数组里面的元素又会重新复制一次。浪费开销,增加效率很低

### LinkedList 
	链表结构 增删快 只需要修改某个节点的prev 和 next只想的信息即可  [每个节点元素存储了前面一个节点的信息 自己的值 和后面一个节点的信息]。但是查找比较慢，只能一个一个的去找 ArrayList直接根据索引去查找即可


### HashMap :key允许为空  通过key的hash值与一些运算确定entry存放的位置 ,在在该位置里面找key 对应的value table用于存放key所对应的索引，线程不安全


### HashTable key不允许为空 为空直接报空指针异常 线程安全的类

### java 泛型的理解
	
	
	
	
	
	
	
	