# 安装java

## 1. 下载jdk
`wget --no-check-certificate --no-cookies --header "Cookie: oraclelicense=accept-securebackup-cookie"  -c
        http://download.oracle.com/otn-pub/java/jdk/8u181-b13/96a7b8442fe848ef90c96a2fad6ed6d1/jdk-8u181-linux-x64.tar.gz`
    
## 2. 解压jdk
`tar -xf jdk-8u181-linux-x64.tar.gz && ln -s jdk1.8.0_181/ java8`

## 3. 配置环境变量

 `vim /etc/profile.d/java.sh`

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
