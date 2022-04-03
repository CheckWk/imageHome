## Linux中安装jdk

#### 	一、通过xftp将压缩包上传到服务器（最好新建一个文件夹名为download）

使用解压指令将文件解压到/usr/local/java/

```shell
tar -zxvf jdk-8u181-linux-x64.tar.gz -C /usr/local/java/
```

#### 二、配置环境变量

1.输入指令编辑etc/profile文件

```shell 
vim /etc/profile #输入指令编辑etc/profile文件
```

2.向文本最后插入以下几行

```shell
export JAVA_HOME=/usr/local/java/jdk1.8.0_161#你的javaJDK的路径
export JRE_HOME=${JAVA_HOME}/jre
export CLASSPATH=.：${JAVA_HOME}/Lib：${JRE_HOME}/Lib
export PATH=${JAVA_HOME}/bin：$PATH
```

3.上面几行添加好后按键盘Esc，在按Shift+：开启键盘输入，输入指令wq保存并退出  （wq保存并退出，q!不保存退出）

![image-20211123171841062](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20211123171841062.png)

4.输入这个指令是让配置文件立即生效

```shell
source /etc/profile
```

#### 三、测试是否成功

输入java 和java  -version能输出信息，就已经成功了

![image-20211123172136808](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20211123172136808.png)

