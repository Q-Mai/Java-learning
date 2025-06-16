# Java的安装

   在甲骨文官网下载[Oracle](https://www.oracle.com/cn/java/technologies/downloads/)

   选择安装路径，**记下安装路径**并安装



# 环境变量的配置

1. 在win中搜索打开**编辑环境变量配置**，点开下方的环境变量

2. 在系统变量一栏中新建变量，变量名为：JAVA_HOME ，变量值为安装Java的路径

3. 打开系统变量中的Path，新建环境变量：%JAVA_HOME%\bin

4. 再新建一个：%JAVA_HOME%\jre\bin

5. 打开CMD ，输入Java -version校验配置是否完成
   
   

## 注意

在新版本Java中并没有jre目录，此时需新建一个jre目录

以管理员身份打开cmd，用cd命令转换到安装目录并执行下列命令

    bin\jlink.exe --module-path jmods --add-modules java.desktop --output jre

此时安装目录就会出现jre目录了


