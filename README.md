## JDK8注释版

### 编译步骤

**1. pull该工程**

**2. 将原来关联的jdk安装目录下的源码src.zip替换成javaJDK8的src**

- 进入路径File -> Project Structure-> Platform Settings -> SDKs -> + ->Add JDK... 

- 为了避免修改原来的SDKs，另外再添加一个名为“javaJDK8”的jdk,并于SourcePath中移除src.zip，添加该项目的src目录

**3.手动将jdk安装目录下lib包中tools.jar添加到项目中**

- 进入路径File -> Project Structure -> Project Settings -> Libraries

- 手动将%JAVA_HOME%/lib/tools.jar添加到项目Library中

**4.编译项目**

- 点击Build -> Build Project编译项目

### 阅读java和javax的之外源代码

我们一般安装的jdk都是SunJDK(OracleJDK)，它只提供java和javax下的源代码，如果我们需要看sun.simc.Launcher这样的类的时候还是没有源代码，我们可以通过下载OpenJDK的源码来查看。

**1.文件准备**

- 找到对应的jdk版本，比如jdk8 http://hg.openjdk.java.net/jdk8/jdk8/jdk/

- 选择左边的zip，下载源码；

- 获得文件jdk-687fd7c7986d.zip

**2.设置 idea**

- 进入路径File -> Project Structure-> Platform Settings -> SDKs -> SourcePath

- 添加之前下载的jdk-687fd7c7986d.zip文件，全选确认

**3.验证**

- 进入sun.simc.Launcher类查看，已能看到注释

### 已添加注释的类

- 暂无