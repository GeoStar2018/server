# 开发环境配置
JMap组件的二次开发环境，也称为GeoGlobeServer RunTime，方便用户使用Java语言调用JMap中基础GIS功能和产品数据集访问能力。
环境配置可以分为两种方式：基于安装包的配置和用户自定义配置。
## Windows环境下配置
### （1）基于安装包的配置
1、安装GeoGlobeServer后，安装过程中已经修改了相关的环境变量，将相关运行环境内容拷贝到指定位置。

2、二次开发只需要将必须的Jar引用到工程项目中，注意使用安装目录下生成的JDK。比如安装目录为：D:\Program Files\GeoGlobe\Server6

3、在新建的Java工程中，可以调用JMap的API接口进行二次开发了。

### （2）用户自定义配置(Windows)
用户自定义配置就是根据提供的开发内容，用户自己配置环境。

（1）二次开发所需内容主要为3部分：
    jdk目录:JDK1.6版本，其中jdk\jre\lib\ext目录下有扩展的Jar。
    support目录：底层GIS内核DLL。
    lib目录：新建Java项目引用jar包。

（2）修改系统环境变量JAVA_HOME
     将原来的JAVA_HOME的指向路径修改为二次开发目录下的jdk目录
     
（3）在系统环境变量中增加对support目录的引用。
     1.增加系统环境变量GEOGLOBESERVER_HOME，内容到support目录的上一级。如： 
     2.PATH路径中增加一条：D:\Program Files\GeoGlobe\Server6\support\native

（4）新建Java工程，引入lib目录下的jar包，就可以开始二次开发了。

## CentOS环境下配置
CentOS环境下配置与Windows环境相类似，只是需要引用的support目录下为一些*.so文件，环境配置不同，
要修改/etc/profile文件内容，在CentOS中需要设置的环境变量如下：

GEOGLOBESERVER_HOME=$USER_INSTALL_DIR$/Server6

CATALINA_HOME=$USER_INSTALL_DIR$/Server6/tomcat

CATALINA_BASE=$USER_INSTALL_DIR$/Server6/tomcat

TOMCAT_HOME=$USER_INSTALL_DIR$/Server6/tomcat

LD_LIBRARY_PATH=$USER_INSTALL_DIR$/Server6/support/native

PATH=$USER_INSTALL_DIR$/Server6/support/native 
