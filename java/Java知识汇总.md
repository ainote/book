# Java

## 基础知识

- 平台无关性
  - [Java如何实现的平台无关性的](http://hollischuang.gitee.io/tobetopjavaer/#/basics/object-oriented/platform-independent?id=%e4%bb%80%e4%b9%88%e6%98%af%e5%b9%b3%e5%8f%b0%e6%97%a0%e5%85%b3%e6%80%a7)
- 多态、继承、封装
  - 什么是多态?动态多态(运行时动态绑定)与静态多态(函数重载)
    - [参考博文](http://hollischuang.gitee.io/tobetopjavaer/#/basics/object-oriented/polymorphism)
  - 方法重载与重写区别
    - [方法重写与重载](http://hollischuang.gitee.io/tobetopjavaer/#/basics/object-oriented/overloading-vs-overriding)
  - 为什么不支持多重继承？(菱形问题)
    - [Java为什么不支持多继承](http://hollischuang.gitee.io/tobetopjavaer/#/basics/object-oriented/multiple-inheritance)
  - 变量、类、方法的作用域
    - [成员变量和方法作用域](http://hollischuang.gitee.io/tobetopjavaer/#/basics/object-oriented/scope)
  - 为什么Java是值传递？可从求值策略角度分析。
    - [值传递、引用传递](http://hollischuang.gitee.io/tobetopjavaer/#/basics/object-oriented/java-pass-by)
    - [为什么说Java中只有值传递](http://hollischuang.gitee.io/tobetopjavaer/#/basics/object-oriented/why-pass-by-reference)
- 基本数据类型
  - Java中为什么byte类型的取值范围为-128~127？
    - [Java中，为什么byte类型的取值范围为-128~127? - CSDN博客](https://blog.csdn.net/qq_23418393/article/details/57421688)
  - 自动拆箱与装箱(基本类型的包装类)
    - [自动拆装箱](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/boxing-unboxing)
  - Integer的缓存机制
    - [Integer的缓存机制](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/integer-cache)
- String
  - JDK1.6与JDK1.7后substring方法的区别？
    - [JDK 6和JDK 7中substring的原理及区别](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/substring)
  - 字符串的几种拼接方式？(concat,StringBuffer,StringBuilder,+)
    - [字符串拼接的几种方式和区别](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/string-concat)
  - int类型转换为字符串的三种方式?
    - [String.valueOf和Integer.toString的区别](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/value-of-vs-to-string)
  - String的intern方法
    - [intern方法](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/intern)
  - String是否存在长度限制？
    - [String有没有长度限制？](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/length-of-string)
  - String StringBuffer 和 StringBuilder 的区别是什么? String 为什么是不可变的?
    - [String StringBuffer 和 StringBuilder 的区别是什么? String 为什么是不可变的?](https://github.com/Snailclimb/JavaGuide/blob/master/docs/java/basis/Java%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86.md#241-string-stringbuffer-%E5%92%8C-stringbuilder-%E7%9A%84%E5%8C%BA%E5%88%AB%E6%98%AF%E4%BB%80%E4%B9%88-string-%E4%B8%BA%E4%BB%80%E4%B9%88%E6%98%AF%E4%B8%8D%E5%8F%AF%E5%8F%98%E7%9A%84)  
- 关键字
  - switch关键字原理
    - [switch对String的支持](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/switch-string)
    - [switch对枚举的支持](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/enum-switch)
  - transient关键字
    - [transient](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/transient-in-java)
  - static 关键字
    - [关于Java的静态：静态类、静态方法、静态变量、静态块等](https://zhuanlan.zhihu.com/p/26819685)
- 补充知识
  > final,static,this,super关键字
  - [Java常用关键字总结](https://github.com/Snailclimb/JavaGuide/blob/master/docs/java/basis/Java%E5%B8%B8%E8%A7%81%E5%85%B3%E9%94%AE%E5%AD%97%E6%80%BB%E7%BB%93.md#static-%E5%85%B3%E9%94%AE%E5%AD%97)

## 集合类

![集合继承关系](../img/java/2021-04-14-13-15-58.png)引用：<https://www.javatpoint.com/collections-in-java>

- Collection和Collections区别?
  - [Collection和Collections区别](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/Collection-vs-Collections)
- Set,List,Map接口的区别?
  - [Set和List区别？](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/set-vs-list)
  - [三大集合：List、Map、Set的区别与联系](https://blog.csdn.net/yangxingpa/article/details/81023138?utm_medium=distribute.pc_relevant_t0.none-task-blog-2%7Edefault%7EBlogCommendFromMachineLearnPai2%7Edefault-1.control&dist_request_id=&depth_1-utm_source=distribute.pc_relevant_t0.none-task-blog-2%7Edefault%7EBlogCommendFromMachineLearnPai2%7Edefault-1.control)
- List 接口
  - ArrayList和LinkedList和Vector的区别
    >分析要点：
    >1.数据结构角度,插入删除元素位置的影响
    >2.扩容角度
    >3.线程安全性角度
    >4.内存占用空间
    >5.快速随机访问
    - [Arraylist 与 LinkedList 区别?](https://github.com/Snailclimb/JavaGuide/blob/master/docs/java/collection/ArrayList%E6%BA%90%E7%A0%81%2B%E6%89%A9%E5%AE%B9%E6%9C%BA%E5%88%B6%E5%88%86%E6%9E%90.md#12-arraylist-%E4%B8%8E-linkedlist-%E5%8C%BA%E5%88%AB)
    - [Arraylist 和 Vector 的区别?](https://github.com/Snailclimb/JavaGuide/blob/master/docs/java/collection/ArrayList%E6%BA%90%E7%A0%81%2B%E6%89%A9%E5%AE%B9%E6%9C%BA%E5%88%B6%E5%88%86%E6%9E%90.md#11-arraylist-%E5%92%8C-vector-%E7%9A%84%E5%8C%BA%E5%88%AB)
    - [ArrayList和LinkedList和Vector的区别](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/arraylist-vs-linkedlist-vs-vector)
  - SynchronizedList和Vector同样线程安全,有什么区别？
    - [SynchronizedList和Vector的区别](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/synchronizedlist-vector)
  - ArrayList扩容机制分析
    - [ArrayList 扩容机制分析](https://github.com/Snailclimb/JavaGuide/blob/master/docs/java/collection/ArrayList%E6%BA%90%E7%A0%81%2B%E6%89%A9%E5%AE%B9%E6%9C%BA%E5%88%B6%E5%88%86%E6%9E%90.md#3-arraylist-%E6%89%A9%E5%AE%B9%E6%9C%BA%E5%88%B6%E5%88%86%E6%9E%90)
- Map接口
  - HashMap和HashTable有何不同？
    - [HashMap和HashTable有何不同？](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/HashMap-HashTable-ConcurrentHashMap)  
    - [HashMap与HashTable的区别](https://hub.fastgit.org/Snailclimb/JavaGuide/blob/master/docs/java/collection/Java%E9%9B%86%E5%90%88%E6%A1%86%E6%9E%B6%E5%B8%B8%E8%A7%81%E9%9D%A2%E8%AF%95%E9%A2%98.md#141-hashmap-%E5%92%8C-hashtable-%E7%9A%84%E5%8C%BA%E5%88%AB)
  - HashMap 和 HashSet 区别
    - [HashMap 和 HashSet 区别](https://hub.fastgit.org/Snailclimb/JavaGuide/blob/master/docs/java/collection/Java%E9%9B%86%E5%90%88%E6%A1%86%E6%9E%B6%E5%B8%B8%E8%A7%81%E9%9D%A2%E8%AF%95%E9%A2%98.md#142-hashmap-%E5%92%8C-hashset-%E5%8C%BA%E5%88%AB)  
  - HashMap 和 TreeMap 区别
    - [HashMap 和 TreeMap 区别](https://hub.fastgit.org/Snailclimb/JavaGuide/blob/master/docs/java/collection/Java%E9%9B%86%E5%90%88%E6%A1%86%E6%9E%B6%E5%B8%B8%E8%A7%81%E9%9D%A2%E8%AF%95%E9%A2%98.md#143-hashmap-%E5%92%8C-treemap-%E5%8C%BA%E5%88%AB)
  - HashMap中数据域的概念解析
    - [HashMap中傻傻分不清楚的那些概念](https://www.hollischuang.com/archives/2416)  
  - HashMap中hash方法的原理
    - [HashMap中hash方法的原理](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/hash-in-hashmap)  
  - 为什么HashMap的默认容量设置成16?
    - [为什么HashMap的默认容量设置成16](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/hashmap-default-capacity)
  - 为什么HashMap的默认负载因子设置成0.75?
    - [为什么HashMap的默认负载因子设置成0.75](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/hashmap-default-loadfactor)
  - 为什么建议设置HashMap的初始容量，设置多少合适
    - [为什么建议设置HashMap的初始容量，设置多少合适](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/hashmap-init-capacity)
  - HashMap 的长度为什么是 2 的幂次方?
    - [HashMap 的长度为什么是 2 的幂次方](https://hub.fastgit.org/Snailclimb/JavaGuide/blob/master/docs/java/collection/Java%E9%9B%86%E5%90%88%E6%A1%86%E6%9E%B6%E5%B8%B8%E8%A7%81%E9%9D%A2%E8%AF%95%E9%A2%98.md#146-hashmap-%E7%9A%84%E9%95%BF%E5%BA%A6%E4%B8%BA%E4%BB%80%E4%B9%88%E6%98%AF-2-%E7%9A%84%E5%B9%82%E6%AC%A1%E6%96%B9)  
  - HashMap 多线程操作导致死循环问题
    - [疫苗：JAVA HASHMAP的死循环](https://coolshell.cn/articles/9606.html)
  - HashMap 有哪几种常见的遍历方式?
    - [HashMap 的 7 种遍历方式与性能分析](https://mp.weixin.qq.com/s/Zz6mofCtmYpABDL1ap04ow)
  - ConcurrentHashMap 和 Hashtable 的区别
    - [ConcurrentHashMap 和 Hashtable 的区别](https://hub.fastgit.org/Snailclimb/JavaGuide/blob/master/docs/java/collection/Java%E9%9B%86%E5%90%88%E6%A1%86%E6%9E%B6%E5%B8%B8%E8%A7%81%E9%9D%A2%E8%AF%95%E9%A2%98.md#149-concurrenthashmap-%E5%92%8C-hashtable-%E7%9A%84%E5%8C%BA%E5%88%AB)
  - ConcurrentHashMap 线程安全的具体实现方式
    - [ConcurrentHashMap 线程安全的具体实现方式/底层具体实现](https://github.com/Snailclimb/JavaGuide/blob/master/docs/java/collection/Java%E9%9B%86%E5%90%88%E6%A1%86%E6%9E%B6%E5%B8%B8%E8%A7%81%E9%9D%A2%E8%AF%95%E9%A2%98.md#1410-concurrenthashmap-%E7%BA%BF%E7%A8%8B%E5%AE%89%E5%85%A8%E7%9A%84%E5%85%B7%E4%BD%93%E5%AE%9E%E7%8E%B0%E6%96%B9%E5%BC%8F%E5%BA%95%E5%B1%82%E5%85%B7%E4%BD%93%E5%AE%9E%E7%8E%B0)  
  - 如何在遍历的同时删除ArrayList中的元素
    - [如何在遍历的同时删除ArrayList中的元素](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/delete-while-iterator)  
- Set接口
  - Set如何保证元素不重复?
    - [Set如何保证元素不重复?](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/set-repetition)  
  - 比较 HashSet、LinkedHashSet 和 TreeSet 三者的异同
    - [比较 HashSet、LinkedHashSet 和 TreeSet 三者的异同](https://hub.fastgit.org/Snailclimb/JavaGuide/blob/master/docs/java/collection/Java%E9%9B%86%E5%90%88%E6%A1%86%E6%9E%B6%E5%B8%B8%E8%A7%81%E9%9D%A2%E8%AF%95%E9%A2%98.md#133-%E6%AF%94%E8%BE%83-hashsetlinkedhashset-%E5%92%8C-treeset-%E4%B8%89%E8%80%85%E7%9A%84%E5%BC%82%E5%90%8C)  
  - HashSet如何判断元素是否重复?
    - [HashSet 如何检查重复](https://hub.fastgit.org/Snailclimb/JavaGuide/blob/master/docs/java/collection/Java%E9%9B%86%E5%90%88%E6%A1%86%E6%9E%B6%E5%B8%B8%E8%A7%81%E9%9D%A2%E8%AF%95%E9%A2%98.md#144-hashset-%E5%A6%82%E4%BD%95%E6%A3%80%E6%9F%A5%E9%87%8D%E5%A4%8D)
    - 扩充知识：[Java hashCode() 和 equals()的若干问题解答](https://www.cnblogs.com/skywang12345/p/3324958.html)  
- 其他
  - Arrays.asList 方法使用注意事项
    - [Arrays.asList获得的List使用时需要注意什么](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/Arrays-asList)
    - [Arrays.asList(T...)](https://hub.fastgit.org/Snailclimb/JavaGuide/blob/master/docs/java/JAD%E5%8F%8D%E7%BC%96%E8%AF%91tricks.md#arraysaslistt)
  - fail-fast 和 fail-safe
    - [fail-fast 和 fail-safe](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/fail-fast-vs-fail-safe)
  - 部分集合源码分析
    - ArrayList源码(JDK1.8)
      - [ArrayList源码+扩容机制分析](https://github.com/Snailclimb/JavaGuide/blob/master/docs/java/collection/ArrayList%E6%BA%90%E7%A0%81%2B%E6%89%A9%E5%AE%B9%E6%9C%BA%E5%88%B6%E5%88%86%E6%9E%90.md)
    - HashMap源码(JDK1.8)  
      - [HashMap(JDK1.8)源码+底层数据结构分析](https://github.com/Snailclimb/JavaGuide/blob/master/docs/java/collection/HashMap(JDK1.8)%E6%BA%90%E7%A0%81%2B%E5%BA%95%E5%B1%82%E6%95%B0%E6%8D%AE%E7%BB%93%E6%9E%84%E5%88%86%E6%9E%90.md)
    - LinkedList源码(JDK1.8)
      - [LinkedList源码分析](https://github.com/Snailclimb/JavaGuide/blob/master/docs/java/collection/LinkedList%E6%BA%90%E7%A0%81%E5%88%86%E6%9E%90.md)
    - ConcurrentHashMap源码
      - [ConcurrentHashMap源码+底层数据结构分析](https://github.com/Snailclimb/JavaGuide/blob/master/docs/java/collection/ConcurrentHashMap%E6%BA%90%E7%A0%81%2B%E5%BA%95%E5%B1%82%E6%95%B0%E6%8D%AE%E7%BB%93%E6%9E%84%E5%88%86%E6%9E%90.md)

## 枚举与注解

- 枚举
  - 枚举的实现原理
    - [JAD反编译tricks#枚举](https://github.com/Snailclimb/JavaGuide/blob/master/docs/java/JAD%E5%8F%8D%E7%BC%96%E8%AF%91tricks.md#%E6%9E%9A%E4%B8%BE)
  - 枚举线程安全及单例实现方式
    - [枚举是如何保证线程安全的](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/enum-serializable?id=%e6%9e%9a%e4%b8%be%e6%98%af%e5%a6%82%e4%bd%95%e4%bf%9d%e8%af%81%e7%ba%bf%e7%a8%8b%e5%ae%89%e5%85%a8%e7%9a%84)
    - [为什么用枚举实现的单例是最好的方式](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/enum-serializable?id=%e4%b8%ba%e4%bb%80%e4%b9%88%e7%94%a8%e6%9e%9a%e4%b8%be%e5%ae%9e%e7%8e%b0%e7%9a%84%e5%8d%95%e4%be%8b%e6%98%af%e6%9c%80%e5%a5%bd%e7%9a%84%e6%96%b9%e5%bc%8f)
  - Java枚举如何比较
    - [Java枚举如何比较](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/enum-compare)
- 注解
  - 注解的实现原理
    - [JAD反编译tricks#注解](https://github.com/Snailclimb/JavaGuide/blob/master/docs/java/JAD%E5%8F%8D%E7%BC%96%E8%AF%91tricks.md#%E6%B3%A8%E8%A7%A3)
  - 元注解包括哪些？
    - [元注解](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/meta-annotation)  
- 扩充知识
  - [用好Java中的枚举真的没有那么简单](https://github.com/Snailclimb/JavaGuide/blob/master/docs/java/basis/%E7%94%A8%E5%A5%BDJava%E4%B8%AD%E7%9A%84%E6%9E%9A%E4%B8%BE%E7%9C%9F%E7%9A%84%E6%B2%A1%E6%9C%89%E9%82%A3%E4%B9%88%E7%AE%80%E5%8D%95.md)
  
## IO流

- Java中IO流的分类
  - [Java 中 IO 流分为几种?](https://github.com/Snailclimb/JavaGuide/blob/master/docs/java/basis/Java%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86.md#341-java-%E4%B8%AD-io-%E6%B5%81%E5%88%86%E4%B8%BA%E5%87%A0%E7%A7%8D)
  - [既然有了字节流,为什么还要有字符流?](https://github.com/Snailclimb/JavaGuide/blob/master/docs/java/basis/Java%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86.md#3411-%E6%97%A2%E7%84%B6%E6%9C%89%E4%BA%86%E5%AD%97%E8%8A%82%E6%B5%81%E4%B8%BA%E4%BB%80%E4%B9%88%E8%BF%98%E8%A6%81%E6%9C%89%E5%AD%97%E7%AC%A6%E6%B5%81)
- BIO,NIO,AIO 有什么区别?
  - [BIO,NIO,AIO 有什么区别?](https://github.com/Snailclimb/JavaGuide/blob/master/docs/java/basis/Java%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86.md#3412-bionioaio-%E6%9C%89%E4%BB%80%E4%B9%88%E5%8C%BA%E5%88%AB)  

## 反射

- 反射的概念、作用、优缺点及应用场景
  - [IOC的实现原理—反射与工厂模式](https://blog.csdn.net/fuzhongmin05/article/details/61614873)

- 动态代理的实现及原理
  - [Jdk动态代理原理解析](https://www.jianshu.com/p/84ffb8d0a338)
  - [代理模式详解](https://github.com/Snailclimb/JavaGuide/blob/master/docs/java/basis/%E4%BB%A3%E7%90%86%E6%A8%A1%E5%BC%8F%E8%AF%A6%E8%A7%A3.md)

## 泛型

- 泛型类型擦除
  - [类型擦除](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/type-erasue?id=%e4%ba%8c%e3%80%81%e4%bb%80%e4%b9%88%e6%98%af%e7%b1%bb%e5%9e%8b%e6%93%a6%e9%99%a4)
- 泛型上下界限定符
  - [上下界限定符extends 和 super](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/extends-vs-super)
  - [限定通配符和非限定通配符](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/Wildcard-Character)
- List<?>和List\<Object>之间的区
  - [List<?>和List\<Object>之间的区](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/genericity-list-wildcard)
  - [List\<Object>和原始类型List之间的区别?](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/genericity-list)
- 补充阅读
  - [聊一聊-JAVA 泛型中的通配符 T，E，K，V，？](https://juejin.cn/post/6844903917835419661#heading-13)

## 异常机制

- Error和Exception的区别
  - [Error和Exception](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/error-vs-exception)
- 异常类型主要包括哪些?受检异常和非受检异常.
  - [异常类型](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/exception-type)
  - [Java异常继承关系、异常类型、try-with-resource、try-catch-finally](https://github.com/Snailclimb/JavaGuide/blob/master/docs/java/basis/Java%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86.md#32-%E5%BC%82%E5%B8%B8)
- try-with-resources 与 try-catch-finally
  - [try-with-resources](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/try-with-resources)
  - [finally和return的执行顺序](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/order-about-finllly-return)

## 其他

- 序列化与反序列化
  - [深入分析Java的序列化与反序列化](https://www.hollischuang.com/archives/1140)
  - [单例与序列化的那些事儿](https://www.hollischuang.com/archives/1144)
- 语法糖
  - [Java中语法糖原理、解语法糖](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/syntactic-sugar)
