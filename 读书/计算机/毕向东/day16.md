# day16

## Map集合

- 该集合中存储键值对，一对一对的往里面存，而且要保证键的唯一性

- 常见操作：

  - 添加

    - put
    - Putall

  - 删除

    - clear
    - Remove

  - 判断

    - containsKey

    - containsValue

      

  - 获取

    - get
    - size
    - Values()
    - entrySet
    - keySet

- 常见：

  - HashTable
    - 底层是哈希表数据结构，不能存入null键null值
    - 该集合是线程同步的
    - jdk1.0 效率低
  - HashMap
    -  底层是哈希表数据结构，并允许使用null键null值，该集合是线程不同步的
    - jdk1.2 效率高
    - 添加元素时，如果出现相同的键，那么后添加的值会覆盖原有键位对应的值，并返回原值。
  - TreeMap
    - 底层是二叉树数据结构，线程不同步，可以给map集合中的键进行排序
    - 和Set很像，Set底层就是使用了Map集合