# Java数据类型拓展

### int（整数型）

定义时可以使用不同的进制（默认为10进制），只需在定义的数字前加特定字符即可

  1.二进制：0b，例：

```java
int i1 = 0b10;
System.out.print(i1);
```

输出结果即为2

2. 八进制：0，例：

```java
int i2 = 011;
System.out.print(i2);
```

输出结果即为9

3. 十六进制：0x，例：

```java
int i3 = 0x17;
System.out.print(i3);
```

输出结果即为23

---

### float与double（浮点类型）

1. float与double两个浮点类型并不相同，所以定义出来的变量就算数值相同比较时也会显示false

例如：

```java
float i1 = 2333.1f;
        double i2 = 2333.1;
        if(i1==i2)
        {
            System.out.println("yes");
        }
        else System.out.println("no");
        System.out.println(i1);
        System.out.println(i2);
```

输出结果为no，但i1与i2输出值都为2333.1

所以要避免使用浮点类型进行比较

2. 浮点类型定义的值是**有限的有理数**，所以在赋予超出其范围或无理数时会自动进行舍入，导致精度下降，此时应该使用Java的数学工具类来处理数据

例如：

```java
float i1 = 1/3f;
System.out.println(i1);
```

输出结果为0.33333334，显然进行了舍入

又如：

```java
   float i3 = 23333333333.1f;
   float i4 = i3 + 1;
   System.out.println(i3);
   System.out.println(i4);
   System.out.println(i3==i4);
```

会发现输出结果为true，但显然i4的值应该要比i3大1才对

**综上，在使用浮点类型时要避免使用浮点类型进行比较与计算**

---

### char（字符类型）

字符类型本质上还是数字，每个字符都有对应的数字表示（Unicode编码），并且可以利用强制类型转换将英文字符类型变为整型（即数字）

例如：

```java
 char i1 = 'a';
 int i2 = i1;
 System.out.println(i1);
 System.out.println(i2);
```

输出结果分别为a与97，97为a的Unicode码位值

```java
char i1 = '中';
int i2 = i1;
System.out.println(i1);
System.out.println(i2);
```

输出结果为“中“与20013，20013即为“中”的Unicode编码码位值


