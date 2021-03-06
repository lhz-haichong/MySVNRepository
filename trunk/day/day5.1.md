# 5.1 第六天日记

## 今日完成工作

* 学习Java 10-11章（进度稍微缓慢，认真学习并且实践 对象和高级类的内容 针对各种状况进行了程序测试，例如 抽象、接口、重载、多态、内部类等）
* 复习SpringMVC

## 相关学习记录

* 为什么需要内部类

    1. 内部类对象可以访问创建它的对象的实现，包括私有数据；
    2. 内部类不为同一包的其他类所见，具有很好的封装性；
    3. 使用内部类可以很方便的编写事件驱动程序；
    4. 匿名内部类可以方便的定义运行时回调；
    5. 内部类可以方便的定义

* 成员内部类

    1. 作为外部类的一个成员存在，与外部类的属性、方法并列。
    1. 成员内部类也是定义在另一个类中，但是定义时不用static修饰。
    1. 成员内部类和静态内部类可以类比为非静态的成员变量和静态的成员变量。
    1. 成员内部类就像一个实例变量。
    1. 它可以访问它的外部类的所有成员变量和方法，不管是静态的还是非静态的都可以。

* 匿名内部类

    1. 匿名内部类不能有构造方法。
    1. 匿名内部类不能定义任何静态成员、方法和类。
    1. 匿名内部类不能是public,protected,private,static。
    1. 只能创建匿名内部类的一个实例。
    1. 一个匿名内部类一定是在new的后面，用其隐含实现一个接口或实现一个类。
    1. 因匿名内部类为局部内部类，所以局部内部类的所有限制都对其生效。

## 今日学习问题

* 抽象类中，在抽象类的构造方法里调用了抽象方法，如果子类实例化过，会调用子类实例化后的方法？

```java
abstract test{
    test(){
        function();
    }

    abstract void function();

    public static void main(String[] args){
        test test = new test();
    }
}

public class my_test extends test{
    my_test(){

    }

    public void function(){
        System.out.println("我是继承类");
    }
}
```

* 关于匿名内部类的方法调用
* 为什么存在匿名内部类，到底比别的好在哪儿

## 发现一个新问题

使用SVN时最好只上传代码部分，将项目的自动生成模块不要commit 如何控制