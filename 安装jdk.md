# 安装java

## 1. 下载jdk
`wget --no-check-certificate --no-cookies --header "Cookie: oraclelicense=accept-securebackup-cookie"  -c
         http://download.oracle.com/otn-pub/java/jdk/8u172-b11/a58eab1ec242421181065cdc37240b08/jdk-8u172-linux-x64.tar.gz`
    
## 2. 解压jdk
`tar -xf jdk-8u172-linux-x64.tar.gz && ln -s jdk1.8.0_172/ java8`

## 3. 配置环境变量

 ` vim /etc/profile.d/java.sh`

```
JAVA_HOME=/usr/local/java8

PATH=$JAVA_HOME/bin:$PATH

CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar

export JAVA_HOME PATH CLASSPATH
```

 `chmod +x /etc/profile.d/java.sh`

 `source /etc/profile.d/java.sh`

 ## 4.验证安装

 `java -version`
