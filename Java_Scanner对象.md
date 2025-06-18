# Scanner对象的使用

通过引入Scanner包来使用

```java
import java.util.Scanner;
```

### 基本语法

```java
Scanner scan = new Scanner(System.in);
```

**想要使用一个类中的方法或参数需要在方法名前面加上类名与.**

---



通过Scanner类的next()与nextLine()方法获取输入的字符串，程序在遇到这两个方法时会等待用户输入数据直到用户按下enter键

```java
String input = scan.next();
```

```java
String input = scan.nextLine():
```

**next()与nextLine()区别在于终止符不同，nextLine()可以获取用户全部的输入文本，以enter为终止符，而next()以空格或enter为终止符，在遇到空格时只会返回空格前的数据**

---



hasNext()与hasNextLine()方法用于判断是否有输入数据并返回一个布尔值

```java
boolean judge = scan.hasNext();
```

```java
boolean judge = scan=hasNextLine();
```

hasNext()与hasNextLine()方法与上面两个一样，在程序遇到时会等待用户输入数据，直到用户按下enter才会继续运行下方的代码，也就是说对于想要让程序继续运行，必须强制用户进行输入操作，并且hasNext()不能识别空格，而hasNextLine()可以



另外，hasNext()与hasNextLine()可以储存输入的内容，也就是会自动将值赋给后面的next()与hasNext()

## 特别注意：凡是属于IO流的类需要关闭，如果不关闭会一直占用资源

```java
scan.close();
```



**Scanner类中还有各种判断输入类型的方法，如hasNextInt()与hasNextDouble()等等**

**要注意的是hasNextDouble()将所有整型与浮点型都视为true，即识别所有数字**

**因为没有专门识别字符的方法，所以可以用非hasNextDouble()来达到识别字符的作用**




