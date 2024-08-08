### 1.查看当前的内核版本
~~~
uname -r
~~~

### 2.安装需要的软件包， yum-util 提供yum-config-manager功能，另两个是devicemapper驱动依赖
~~~
yum install -y yum-utils device-mapper-persistent-data lvm2
~~~

  ### 3.设置一个yum源

~~~ 
yum-config-manager --add-repo http://download.docker.com/linux/centos/docker-ce.repo（中央仓库  网络原因，可能访问不到）

yum-config-manager --add-repo http://mirrors.aliyun.com/docker-ce/linux/centos/docker-ce.repo（阿里仓库）
~~~

### 4.选择docker 版本安装

（1）查看可用的docker版本

~~~ 
yum list docker-ce --showduplicates | sort -r
~~~

（2）选择一个版本并安装

~~~
yum install docker-ce-版本号

yum -y install docker-ce-18.03.1.ce
~~~

（3）启动docker 并设置开机自启

~~~
systemctl start docker
systemctl enable docker
~~~

（4）查看docker状态

~~~
docker version
~~~

