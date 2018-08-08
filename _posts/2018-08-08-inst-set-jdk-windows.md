---
layout: post
title: Windows系统JDK安装与环境变量配置
date: 2018-08-08
categories: blog
tags: [java]
description: Windows系统jdk安装与环境变量配置
---

# Windows系统JDK安装与环境变量配置

---

## 1.下载安装

### 1.1下载

到官网下载对应版本的安装包。

<a href="http://www.oracle.com/technetwork/java/javase/downloads/index.html" target="_blank">http://www.oracle.com/technetwork/java/javase/downloads/index.html</a>

选择Java SE 8u181版本

![java-download1](/img/20180808/java-download1.jpg)

点击DOWNLOAD，链接如下

<a href="http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html" target="_blank">http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html</a>

如图，选择Windows对应的版本进行下载

`Windows x64 202.73 MB   jdk-8u181-windows-x64.exe`

![java-download2](/img/20180808/java-download2.jpg)

下载完成如图：

![java-download-file](/img/20180808/java-download-file.jpg "安装包")

### 1.2安装

**双击安装：**

![java-inst](/img/20180808/java-inst1.jpg "java install")

依次点击下一步，会分别进行`jdk1.8.0`的安装和`jre1.8.0`的安装

![java-inst](/img/20180808/java-inst2.jpg "java install")
![java-inst](/img/20180808/java-inst3.jpg "java install")

**安装完成如下:**

![java-inst](/img/20180808/java-inst4.jpg "java finish")
![java-inst](/img/20180808/java-inst5.jpg "java finish")

默认安装路径为：

**jdk:**

```
C:\Program Files\Java\jdk1.8.0_181
```

**jre:**

```
C:\Program Files\Java\jre1.8.0_181
```

## 2.配置环境变量

在 我的电脑 右键选择 属性，点击 高级系统设置，找到环境变量
![java-set1](/img/20180808/java-set1.jpg)

### 2.1创建系统变量JAVA_HOME

**作用：**它指向jdk的安装目录，Eclipse/NetBeans/Tomcat等软件就是通过搜索JAVA_HOME变量来找到并使用安装好的jdk。

**配置方法：**在系统变量里点击新建，变量名填写`JAVA_HOME`，变量值填写JDK的安装路径（根据自己的安装路径填写）,比如: 

```
C:\Program Files\Java\jdk1.8.0_181
```

![java-set2-1-1](/img/20180808/java-set-javahome.jpg)

### 2.2创建系统变量CLASSPATH

**作用：**是指定类搜索路径，要使用已经编写好的类，前提当然是能够找到它们了，JVM就是通过CLASSPTH来寻找类的。
我们需要把jdk安装目录下的lib子目录中的dt.jar和tools.jar设置到CLASSPATH中，当然，当前目录“.”也必须加入到该变量中。

**配置方法：**在系统变量里点击新建，变量名填写`CLASSPATH`，变量值是

```
.;%JAVA_HOME%\lib;%JAVA_HOME%\lib\dt.jar;%JAVA_HOME%\lib\tools.jar;
```


![java-set2-2-1](/img/20180808/java-set-classpath.jpg)

### 2.3添加path环境变量

**作用：**指定命令搜索路径，在命令行下面执行命令如javac编译java程序时，它会到PATH变量所指定的路径中查找看是否能找到相应的命令程序。我们需要把jdk安装目录下的bin目录增加到现有的PATH变量中，bin目录中包含经常要用到的可执行文件如javac/java/javadoc等待，设置好PATH变量后，就可以在任何目录下执行javac/java等工具了。

**配置方法：**在系统变量里找到Path变量，这是系统自带的，不用新建。双击Path，由于原来的变量值已经存在，故应在已有的变量后加上

```
;%JAVA_HOME%\bin;%JAVA_HOME%\jre\bin
```

注意前面的分号。

![java-set2-3-1](/img/20180808/java-set-path.jpg)

**注意：若为win10，则必须用jdk的绝对路径，而不能用%JAVA_HOME%，计算机识别不了(此时javac会识别不了）。**

**因此，加上的分别是：**

```
C:\Program Files\Java\jdk1.8.0_181\bin
```

和

```
C:\Program Files\Java\jdk1.8.0_181\jre\bin
```

如图所示：

![java-set2-3-2](/img/20180808/java-set-path2.jpg)

## 3.测试环境
检验是否配置成功 运行cmd 分别输入`java`，`javac`， `java -version` （`java` 和 `-version` 之间有空格）。

### 3.1 Java

![java-test-java](/img/20180808/java-test-java.jpg)

### 3.2 Javac

![java-test-javac](/img/20180808/java-test-javac.jpg)

### 3.3 Java –version

![java-test-java-version](/img/20180808/java-test-java-version.jpg)

若如图所示 显示版本信息 则说明安装和配置成功。

也可以在命令行输入`echo %JAVA_HOME%`来查看当前的`JAVA_HOME`路径。

## 小结：

**环境变量：**

`JAVA_HOME`：

```
C:\Program Files\Java\jdk1.8.0_181
```

`CLASSPATH`：

```
.;%JAVA_HOME%\lib;%JAVA_HOME%\lib\dt.jar;%JAVA_HOME%\lib\tools.jar;
```

`Path`：

```
C:\Program Files\Java\jdk1.8.0_181\bin;C:\Program Files\Java\jdk1.8.0_181\jre\bin;
```


**测试：**

`java`，`javac`，`java –version`

---

**References:**

[1] [Windows环境下JDK安装与环境变量配置详细的图文教程](https://www.cnblogs.com/liuhongfeng/p/4177568.html)

[2] [jdk安装与环境变量配置，看这篇就够了](https://blog.csdn.net/shenshizhong/article/details/77391728)

[3] [JDK下载与安装教程](https://blog.csdn.net/u012934325/article/details/73441617)
