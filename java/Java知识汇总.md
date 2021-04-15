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

# 并发与线程安全

## 多线程基本概念

- 线程与进程、并行与并发、线程上下文切换、线程安全
  - [深入理解Java并发编程（一）：到底什么是线程安全](https://www.hollischuang.com/archives/3060)
  - [什么是上下文切换?](https://github.com/Snailclimb/JavaGuide/blob/master/docs/java/multi-thread/2020%E6%9C%80%E6%96%B0Java%E5%B9%B6%E5%8F%91%E5%9F%BA%E7%A1%80%E5%B8%B8%E8%A7%81%E9%9D%A2%E8%AF%95%E9%A2%98%E6%80%BB%E7%BB%93.md#7-%E4%BB%80%E4%B9%88%E6%98%AF%E4%B8%8A%E4%B8%8B%E6%96%87%E5%88%87%E6%8D%A2)
  - [说说并发与并行的区别?](https://github.com/Snailclimb/JavaGuide/blob/master/docs/java/multi-thread/2020%E6%9C%80%E6%96%B0Java%E5%B9%B6%E5%8F%91%E5%9F%BA%E7%A1%80%E5%B8%B8%E8%A7%81%E9%9D%A2%E8%AF%95%E9%A2%98%E6%80%BB%E7%BB%93.md#3-%E8%AF%B4%E8%AF%B4%E5%B9%B6%E5%8F%91%E4%B8%8E%E5%B9%B6%E8%A1%8C%E7%9A%84%E5%8C%BA%E5%88%AB)
- 线程死锁
  - [什么是线程死锁?如何避免死锁?](https://github.com/Snailclimb/JavaGuide/blob/master/docs/java/multi-thread/2020%E6%9C%80%E6%96%B0Java%E5%B9%B6%E5%8F%91%E5%9F%BA%E7%A1%80%E5%B8%B8%E8%A7%81%E9%9D%A2%E8%AF%95%E9%A2%98%E6%80%BB%E7%BB%93.md#8-%E4%BB%80%E4%B9%88%E6%98%AF%E7%BA%BF%E7%A8%8B%E6%AD%BB%E9%94%81%E5%A6%82%E4%BD%95%E9%81%BF%E5%85%8D%E6%AD%BB%E9%94%81)
- 线程状态
  - [说说线程的生命周期和状态?](https://github.com/Snailclimb/JavaGuide/blob/master/docs/java/multi-thread/2020%E6%9C%80%E6%96%B0Java%E5%B9%B6%E5%8F%91%E5%9F%BA%E7%A1%80%E5%B8%B8%E8%A7%81%E9%9D%A2%E8%AF%95%E9%A2%98%E6%80%BB%E7%BB%93.md#6-%E8%AF%B4%E8%AF%B4%E7%BA%BF%E7%A8%8B%E7%9A%84%E7%94%9F%E5%91%BD%E5%91%A8%E6%9C%9F%E5%92%8C%E7%8A%B6%E6%80%81)
- 创建线程的几种方式
  - [创建线程有哪几种方式？](https://zhuanlan.zhihu.com/p/338634085)
- 线程池
  - [线程池相关的问题](https://github.com/Snailclimb/JavaGuide/blob/master/docs/java/multi-thread/2020%E6%9C%80%E6%96%B0Java%E5%B9%B6%E5%8F%91%E8%BF%9B%E9%98%B6%E5%B8%B8%E8%A7%81%E9%9D%A2%E8%AF%95%E9%A2%98%E6%80%BB%E7%BB%93.md#4-%E7%BA%BF%E7%A8%8B%E6%B1%A0)
  - [Java中线程池，你真的会用吗？](https://www.hollischuang.com/archives/2888)
  - [java线程池学习总结](https://github.com/Snailclimb/JavaGuide/blob/master/docs/java/multi-thread/java%E7%BA%BF%E7%A8%8B%E6%B1%A0%E5%AD%A6%E4%B9%A0%E6%80%BB%E7%BB%93.md)

## 线程安全与同步

- 什么是线程安全?
  - [深入理解Java并发编程（一）：到底什么是线程安全](https://www.hollischuang.com/archives/3060)
  - [[译]Java虚拟机是如何执行线程同步的](https://www.hollischuang.com/archives/1876)
- CAS
  - [彻底理解synchronized关键字#CAS操作](https://www.codercc.com/backend/basic/juc/concurrent-keywords/synchronized.html#_3-1-cas%E6%93%8D%E4%BD%9C)
- Java内存模型(JMM)
  - [再有人问你Java内存模型是什么，就把这篇文章发给他](https://www.hollischuang.com/archives/2550)
  - [并发编程——原子性，可见性和有序性](https://blog.csdn.net/eff666/article/details/66473088)
  - [java内存模型以及happens-before规则](https://www.codercc.com/backend/basic/juc/concurrent-theory/jmm-happens-before.html)
  - [内存模型是怎么解决缓存一致性问题的？](https://www.hollischuang.com/archives/2662)
- synchronized关键字
  - synchronized关键字的使用
    - [synchronized 关键字最主要的三种使用方式](https://github.com/Snailclimb/JavaGuide/blob/master/docs/java/multi-thread/2020%E6%9C%80%E6%96%B0Java%E5%B9%B6%E5%8F%91%E8%BF%9B%E9%98%B6%E5%B8%B8%E8%A7%81%E9%9D%A2%E8%AF%95%E9%A2%98%E6%80%BB%E7%BB%93.md#12-%E8%AF%B4%E8%AF%B4%E8%87%AA%E5%B7%B1%E6%98%AF%E6%80%8E%E4%B9%88%E4%BD%BF%E7%94%A8-synchronized-%E5%85%B3%E9%94%AE%E5%AD%97)
  - synchronized实现原理
    - [深入理解多线程（一）——Synchronized的实现原理](https://www.hollischuang.com/archives/1883)
    - [深入理解多线程（四）—— Moniter的实现原理](https://www.hollischuang.com/archives/2030)
    - [彻底理解synchronized关键字](https://www.codercc.com/backend/basic/juc/concurrent-keywords/synchronized.html)
  - synchronized锁优化
    - [Java6及以上版本对synchronized的优化](https://www.cnblogs.com/wuqinglong/p/9945618.html)
    - [彻底理解synchronized关键字#synchronized优化](https://www.codercc.com/backend/basic/juc/concurrent-keywords/synchronized.html#_3-synchronized%E4%BC%98%E5%8C%96)
    - [深入理解多线程（五）—— Java虚拟机的锁优化技术](https://www.hollischuang.com/archives/2344)
  - synchronized与原子性、有序性、可见性
    - [再有人问你synchronized是什么，就把这篇文章发给他](https://www.hollischuang.com/archives/2637)
- volatile关键字
  - [深入理解Java中的volatile关键字](https://www.hollischuang.com/archives/2648)
  - [彻底理解volatile关键字](https://www.codercc.com/backend/basic/juc/concurrent-keywords/volatile.html)
  - [深入理解 Java 内存模型（四）——volatile](https://www.infoq.cn/article/java-memory-model-4/)
- final关键字
  - [深入理解 Java 内存模型（六）——final](https://www.infoq.cn/article/java-memory-model-6?utm_source=related_read_bottom&utm_medium=article)
  - [你以为你真的了解final吗](https://www.codercc.com/backend/basic/juc/concurrent-keywords/final.html)
- 补充阅读
  - [深入理解 Java 内存模型（一）——基础](https://www.infoq.cn/article/java-memory-model-1)
  - [深入理解 Java 内存模型（二）——重排序](https://www.infoq.cn/article/java-memory-model-2)
  - [深入理解 Java 内存模型（三）——顺序一致性](https://www.infoq.cn/article/java-memory-model-3)
  - [深入理解 Java 内存模型（四）——volatile](https://www.infoq.cn/article/java-memory-model-4)
  - [深入理解 Java 内存模型（五）——锁](https://www.infoq.cn/article/java-memory-model-5)
  - [深入理解 Java 内存模型（六）——final](https://www.infoq.cn/article/java-memory-model-6)
  - [深入理解 Java 内存模型（七）——总结](https://www.infoq.cn/article/java-memory-model-7)
- Lock与AQS(AbstractQueuedSynchronizer)
  - Lock与AQS概念
    - [初识Lock与AbstractQueuedSynchronizer(AQS)](https://www.codercc.com/backend/basic/juc/lock/Lock-AbstractQueuedSynchronizer.html)
    - [深入理解AQS](https://www.codercc.com/backend/basic/juc/lock/AbstractQueuedSynchronizer-theory.html)
  - ReentrantLock
    - [深入理解ReentrantLock](https://www.codercc.com/backend/basic/juc/lock/ReentrantLock.html#_1-reentrantlock%E7%9A%84%E4%BB%8B%E7%BB%8D)
  - ReentrantReadWriteLock
    - [深入理解ReentrantReadWriteLock](https://www.codercc.com/backend/basic/juc/lock/ReentrantReadWriteLock.html) 
  - Condition
    - [详解Condition](https://www.codercc.com/backend/basic/juc/lock/condition.html)
  - LockSupport
    - [LockSupport工具](https://www.codercc.com/backend/basic/juc/lock/LockSupport.html)
  - CountDownLatch与CyclicBarrier
    - [大白话说java并发工具类-CountDownLatch，CyclicBarrier](https://www.codercc.com/backend/basic/juc/concurrent-util/CountDownLatch-CyclicBarrier.html)
  - Semaphore与Exchanger
    - [大白话说java并发工具类-Semaphore，Exchanger](https://www.codercc.com/backend/basic/juc/concurrent-util/Semaphore-Exchanger.html)  
- 并发容器
  - ConcurrentHashMap
    - [深入理解ConcurrentHashMap(1.8)](https://www.codercc.com/backend/basic/juc/concurrent-container/ConcurrentHashMap.html)
  - CopyOnWriteArrayList
    - [深入理解CopyOnWriteArrayList](https://www.codercc.com/backend/basic/juc/concurrent-container/CopyOnWriteArrayList.html)
  - ConcurrentLinkedQueue
    - [深入理解ConcurrentLinkedQueue](https://www.codercc.com/backend/basic/juc/concurrent-container/ConcurrentLinkedQueue.html)
  - ThreadLocal
    - [深入理解ThreadLocal](https://www.codercc.com/backend/basic/juc/concurrent-container/ThreadLocal.html)
    - [深入理解ThreadLocal内存泄漏](https://www.codercc.com/backend/basic/juc/concurrent-container/threadlocal-memory-leak.html)
  - BlockingQueue
    - [阻塞队列汇总](https://www.codercc.com/backend/basic/juc/concurrent-container/BlockingQueue.html)
    - [深入理解ArrayBlockingQueue和LinkedBlockingQueue](https://www.codercc.com/backend/basic/juc/concurrent-container/ArrayBlockingQueue-LinkedBlockingQueue.html)
- Atomic
  - 原子操作类总结
    - [Java中atomic包中的原子操作类总结](https://www.codercc.com/backend/basic/juc/atomic/atomic-util.html)

## JVM

- Java内存区域(运行时数区域)
  - [Java运行时数据区域](https://github.com/Snailclimb/JavaGuide/blob/master/docs/java/jvm/Java%E5%86%85%E5%AD%98%E5%8C%BA%E5%9F%9F.md#%E4%BA%8C-%E8%BF%90%E8%A1%8C%E6%97%B6%E6%95%B0%E6%8D%AE%E5%8C%BA%E5%9F%9F)
  - [大白话带你认识JVM#运行时数据区](https://juejin.cn/post/6844904048013869064#heading-18)
  - 扩展阅读
    - [对象和数组并不是都在堆上分配内存的。](https://www.hollischuang.com/archives/2398)
    - [万万没想到，JVM内存结构的面试题可以问的这么难？](https://www.hollischuang.com/archives/3875)
- HotSpot虚拟机对象
  >对象创建过程  
  >对象内存布局  
  >对象访问定位
  [HotSpot 虚拟机对象探秘](https://github.com/Snailclimb/JavaGuide/blob/master/docs/java/jvm/Java%E5%86%85%E5%AD%98%E5%8C%BA%E5%9F%9F.md#%E4%B8%89-hotspot-%E8%99%9A%E6%8B%9F%E6%9C%BA%E5%AF%B9%E8%B1%A1%E6%8E%A2%E7%A7%98)
- 类加载器
  - [深度分析Java的ClassLoader机制（源码级别）](https://www.hollischuang.com/archives/199)
  - [Java类的加载、链接和初始化](https://www.hollischuang.com/archives/201)
  - [类加载过程](https://github.com/Snailclimb/JavaGuide/blob/master/docs/java/jvm/%E7%B1%BB%E5%8A%A0%E8%BD%BD%E8%BF%87%E7%A8%8B.md)
  - [双亲委派机制详解(我竟然被”双亲委派”给虐了！)](https://www.hollischuang.com/archives/6055)
- Class类文件结构
  - [Class类文件结构详解](https://github.com/Snailclimb/JavaGuide/blob/master/docs/java/jvm/%E7%B1%BB%E6%96%87%E4%BB%B6%E7%BB%93%E6%9E%84.md)
- Class常量池、字符串常量池及运行时常量池
  - [《Java虚拟机原理图解》 1.2.2、Class文件中的常量池详解（上）](https://blog.csdn.net/luanlouis/article/details/39960815)
  - [Java基础-JVM内存管理-常量池与运行时常量池](https://www.jianshu.com/p/e49bab4e44a6)
