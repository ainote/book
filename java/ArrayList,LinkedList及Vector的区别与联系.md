# 1. 引言

本文从以下几个角度分析ArrayList,LinkedList,Vector的异同及联系。
（1）相同点。
（2）底层数据存储结构
（3）数据插入、删除和读取操作的异同
（4）扩容角度
（5）线程安全性角度
（6）内存占用情况
（7）是否支持快速随机访问

## 2. 相同点

ArrayList,LinkedList,Vector三者都是List接口的实现类。遵循List接口的特性，即存储的数据是有序的。

## 3. 底层数据存储结构

ArrayList的底层数据存储采用的`数组`。数组的类型为Object，需要注意的是数组使用了关键字transient进行了修饰,[ArrayList使用了transient关键字进行存储优化，而Vector没有，为什么？](http://hollischuang.gitee.io/tobetopjavaer/#/basics/java-basic/why-transient-in-arraylist)

```Java
/**
     * The array buffer into which the elements of the ArrayList are stored.
     * The capacity of the ArrayList is the length of this array buffer. Any
     * empty ArrayList with elementData == DEFAULTCAPACITY_EMPTY_ELEMENTDATA
     * will be expanded to DEFAULT_CAPACITY when the first element is added.
     */
    transient Object[] elementData; // non-private to simplify nested class access
```

Vector的底层数据存储采用`数组`。数组的类型为Object。

```Java
/**
     * The array buffer into which the components of the vector are
     * stored. The capacity of the vector is the length of this array buffer,
     * and is at least large enough to contain all the vector's elements.
     *
     * <p>Any array elements following the last element in the Vector are null.
     *
     * @serial
     */
    protected Object[] elementData;
```

LinkedList底层采用的数据结构是`双向链表`.注意在JDK1.6之前采用是`循环双向列表`，在JDK1.7后取消了循环采用`双向链表`. 其内部的`Node`节点分别使用`prev`和`next`指向前一个节点和后一个节点。另外，LinkedList除了实现`List`接口外，还实现了`Deque`接口以实现队列的功能。

```Java
// JDK1.8 
private static class Node<E> {
        E item;
        Node<E> next; // 下一个节点
        Node<E> prev; // 上一个节点

        Node(Node<E> prev, E element, Node<E> next) {
            this.item = element;
            this.next = next;
            this.prev = prev;
        }
    }
```

## 4. 数据插入、删除和读取操作的异同

### 4.1 数据插入

ArrayList集合数据写入常用的方法是add,该方法是一个重载方法提供了两个不同的参数：

```Java
/* 在数据末尾新增一个数据 */
public boolean add(E e)

/* 在指定的数组下标插入数据 */
public void add(int index, E element)

```

这两个方法的实现过程基本是一致的：
（1）使用 `ensureCapacityInternal(size + 1)`方法检测数组容量
（2）将元素写入插入到数组中。
> `add(E e)`方法：直接在数组末尾追加，时间复杂度为O(1)。
> `add(int index, E element)`方法：通过System.arraycopy方法将指定下标后面的元素向后移动，然后将数据插入到指定的下标位置，时间复杂度为O(n).

LinkedList作为列表集合使用时，同样是通过add方法插入元素,该方法同样提供了两个不同的参数：

```Java
/* 在末尾插入元素 */
public boolean add(E e)

/* 在指定的下标插入数据 */
public void add(int index, E element)
```
