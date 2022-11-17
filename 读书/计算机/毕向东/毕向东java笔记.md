# day14 

## 多态在实际编程中的应用

成员变量，静态方法看左边；

非静态方法：编译看左边，运行看右边

”意思是：当父类变量引用子类对象时（Fu f = new Zi();

），在这个引用变量f指向的对象中，他的成员变量和静态方法与父类是一致的，他的非静态方法，在编译时是与父类一致的，运行时却与子类一致（发生了复写）。

[java中的多态和继承---"编译看左边，运行看右边"（多态执行）【转】 - 鱼笑笑 - 博客园 (cnblogs.com)](https://www.cnblogs.com/efforts-will-be-lucky/p/7118685.html)

[java问题（多态中编译看左边，运行看右边） - 简书 (jianshu.com)](https://www.jianshu.com/p/3d69236d198c)

```java

class Zi extends Fu {

    int num = 8;

    static void method4() {

        System.out.println("zi method_4");

    }

    void method3() {

        System.out.println("zi method_3");

    }

}

class DuoTaiDemo4 {

    public static void main(String[] args) {

        Fu f = new Zi();

        System.out.println(f.num);//与父类一致

        f.method4();//与父类一致

        f.method3();//编译时与父类一致，运行时与子类一致

        Ziz = new Zi();

        System.out.println(z.num);

        z.method4();

        z.method3();

    }

}

输出结果：

        5

        fu method_4

        zi method_3

        8

        zi method_4

        zi method_3
```

