# File

## 创建

1. boolean createNewFile()

   - 在指定位置位置创建文件，如果该文件已经存在，则不创建，返回false

   - 和输出流不一样，输出流对象一建立创建文件夹。而且如果文件已经存在会覆盖


2. boolean mkdir()
   - 创建文件夹


3.  boolean mkdirs()
    - 创建多级文件夹


## 删除

1. boolean delete()
   - 删除失败返回false，删除成功返回true。如果文件被占用返回false


2. void deleteOnExit()
   - 虚拟机退出时删除指定文件


## 判断

1. boolean exists()
   - 判断文件是否存在


2. isFile()

3. isDirrectory()

4. isHidden()

5. isAbsolute()

## 获取信息

1. String getName()

2. String getPath()

3. String getParent()

4. String getAbsolutePath()

5. long length()

6. long lastModified()

7. File[] listFile()
   - 获取指定文件夹下的文件文件夹的File对象数组


8. String list()
   - 获取指定文件夹下的所有文件文件夹的名字字符串


## 递归

> 列出指定目录下文件或者文件夹，包含子目录中的内容。也就是列出指定目录下所有内容。因为目录中还有目录，只要使用同一个列出目录功能的函数完成即可。在列出过程中出现的还是目录的话，还可以再次调用本功能。也就是函数自身调用自身。这种表现形式，或者编程手法，称为递归。

> 递归要注意：
>
> ee
>
> 1，限定条件。
>
> 2，要注意递归的次数。尽量避免内存溢出。

```java
```

