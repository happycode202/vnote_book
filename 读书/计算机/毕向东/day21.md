# day21

# io包中的其他类

- 操作对象
  - ObjectOutputStream和ObjectInputStream
    - 被操作的对象需要实现Serializable(标记接口)，没有方法需要被实现，只做标记
- 管道流
  - PipeInputStream和PipeOutputStream
    - 输入输出可以直接进行连接，通常结合线程使用
- 随机访问文件
  - RandomAccessFile
    - 该类不算是IO体系中的子类，该类直接继承自Object。但是它是IO包中的成员。因为它具备读写功能。内不封装了一个数组，而且通过指针对数据的元素进行操作，可以通过getFilePointer获取指针的位置。同时可以通过seek改变指针的位置
    - 其实完成读写的原理就是内部封装了字节输入流和输出流。
    - 通过构造函数可以看出，该类只能操作文件，而且，操作文件还有模式，比如'r''rw'
    - 该对象的构造函数要操作的文件如果不存在会自动创建。如果存在会覆盖。
    - 如果模式为r，不会创建文件，会去读取一个已存在的文件，如果文件不存在，会出现异常。
    - 如果模式为rw，操作文件如果不存在会创建，存在会覆盖
    - 