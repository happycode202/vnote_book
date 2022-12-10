# day20

## File类常见方法

1. 创建

   1. boolean createNewFile(); 在指定位置创建文件，如果该文件已经存在，则不创建，返回false。和输出流不一样，输出流对象一建立就创建文件。如果文件已存在，会覆盖原文件

      ```java
      File f=new File("demo.txt")
      f.createNewFile();		
      ```

   2. Boolean mkdir():创建目录，只能创建一级目录

      ```
      file dir=New File("adc")
      dir.mkdir();
      ```

      

   3. Boolean mkdirs();创建多级文件夹

      ```java
      File dir=new File("abc\\bc\\b");
      dir.mkdirs();
      ```

      

2. 删除

   1. Boolean delete()；删除失败返回false
   
3. 判断

   1. Boolean exists();文件是否存在
   2. Boolean canExecute();文件是否可执行，针对java虚拟机
   3. isDirectory();
   4. isFile();
   5. isAbsolute();判断路径名是否是绝对路径
   
4. 获取
   1. String getName();
   2. getPath();封装的是什么路径获取的就是什么。封装的绝对路径获取的就是绝对的，封装的是相对的，获取的就是相对的；
   3. getParent();该方法获取的是
   4. String getAbsolutePath(); 该方法返回的是绝对路径中的父目录。如果获取的是相对路径，返回地是null。如果相对路径中有上级目录，则返回上级目录。
   5. File getAbsoluteFile();获取绝对路径对应的文件对象。
   6. long length();获取文件大小
   7. long lastModified()；最后一次修改时间
   8. renameTo();重命名，剪切
   9. list();指定路径下的所有文件和文件夹名称，返回string[] names
   10. String[] list(FilenameFilter filter);返回指定路径下的所有文件的名字
   11. File[] listFiles();返回文件目录下所有文件文件夹的file对象数组。
   12. listRoots();返回根目录的路径，如果是windows则返回各个盘符的根目录
   13. 

## 递归

- 例子：

- 列出指定目录下文件或者文件夹，包含目录中的内容。也就是列出指定目录下的所有内容

  ```java
  	public class FileDemo4 {
      public static void main(String[] args) throws IOException {
          File file = new File("/Users/sunhl/Downloads/rime-ice");
          List<File> list = new ArrayList<>();
          List<File> dir = getDir(file, list);
  
          //输出到到文件，使用fileWriter
          //高速写出，需要使用buffer
          BufferedWriter bufw = new BufferedWriter(new FileWriter("/Users/sunhl/Downloads/test/demo.txt"));
          //将结果输出到控制台上
          //将list集合中的数据取出，并输出到控制台
          for (File f : dir) {
  //            System.out.println(f);
  //            将结果输出到文件
              //写入f的绝对地址值
              bufw.write(f.getAbsolutePath());
              //新行
              bufw.newLine();
              //刷新缓冲区
              bufw.flush();
          }
          //关闭流
          bufw.close();
      }
  
      public static List<File> getDir(File file, List<File> list) {
          File[] files = file.listFiles();
          for (File f : files) {
              if (f.isDirectory()) {
                  getDir(f,list);
              } else
                  list.add(f);
          }
          return list;
      }
  }
  ```


## Properties

- Properties是hashtable的子类。
- 也就是说它具备map集合的特点，而且，它里面存储的键值对都是字符串
- 是集合中和io技术相结合的集合容器
- 该对象的特点：可以用于键值对形式的配置文件

## 打印流



> 该流提供了打印的方法，可以将各种数据类型的数据都原样打印。

1. 字节打印流：PrintStream
   - 构造函数可以接收的参数类型
     - File对象：File
     - 字符串路径：String
     - 字节输出流：OutputStream
2. 字符打印流：PrintWriter
   - 构造函数可以接收的参数类型
     - File对象：File
     - 字符串路径：String
     - 字节输出流：OutputStream
     - 字符输出流：Writer
3. 