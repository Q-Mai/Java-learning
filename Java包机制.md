# Java的包机制（相当于装类的文件夹，可以使两个不同的包中拥有相同命名的文件）

用于区别类名的命名空间



一般利用公司域名倒置作为包名：

例如：

```java
package com.baidu.wwww;
```

想要使用其他包的成员，需要在程序中导入该包，使用import导入

```java
import package1;
```

如果要用其他包的实例变量，需要在定义实例变量时加上修饰符public

```java
public int norm = 3;
```
