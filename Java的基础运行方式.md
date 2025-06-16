# Java的基础运行方式

在java文件位置下启动cmd，并使用javac编译文件

    javac + 文件名.java

编译完成后文件夹下会多生成一个编译好的class文件，此时使用java来运行它

    java + 文件名

注意此时不需要加后缀



## 容易犯的几个错误

1. Java严格区分大小写，一些关键语句是需要区分大小写的，如String类

2. 文件名与类名必须完全一致，即文件名要与class后的类名要相同
   
   ```java
   public class 文件名
   ```
