---
title: ubuntu 把 OPENJDK 换成 JDK
tags: ["linux"]
---

参考文献：http://blog.sina.com.cn/s/blog_493e1d510102vonv.html

由于ubuntu中可能会有默认的jdk，如openjdk。假如有openjdk的话，结果还是OpenJDK。

所以，为了使默认使用的是我们安装的jdk，还要进行如下工作。
执行
代码:
```shell
update-alternatives --install /usr/bin/java java  usr/java/jdk1.8.0_45/bin/java 300
update-alternatives --install /usr/bin/javac javac usr/java/jdk1.8.0_45/bin/javac 300
```
通过这一步将我们安装的jdk加入java选单。

然后执行
代码:
```shell
update-alternatives --config java
```
