---
typora-root-url: D:\github\tech_exp\images
---

~~~ 1、报错：git@github.com:liuhanchang/tech_exp.git
使用sourcetree提交github报错：Support for password authentication was removed on August 13, 2021. 
~~~

#### 一、使用git生成公私钥

##### 1、在Git bash中输入如下内容：如果没有Git bash需要下载一个Git bash。

 `git config --global user.name "871458219@qq.com"`

`git config --global user.email "871458219@qq.com"`
##### 2、生成ssh密钥
`ssh-keygen -t rsa -C "871458219@qq.com"`
显示结果如下所示：

![img](https://i-blog.csdnimg.cn/blog_migrate/cb0ed28b380675b75696a367b5dd951b.png)

##### 3、检查密钥生成
最终，在您的电脑本地/c/Users/hanchang.liu/.ssh/id_rsa文件夹中可见：

[![](/image-20240808104750578.png)](https://github.com/liuhanchang/tech_exp/blob/main/images/image-20240808104750578.png)

#### 三、在soure tree添加SSH Key
##### 1、点击工具 -> 选项

[![](/image-20240808104846185.png)](https://github.com/liuhanchang/tech_exp/blob/main/images/image-20240808104846185.png)



##### 2、配置OpenSSH客户端

#### 四、配置github服务器

1. 登录github服务器， https://github.com/settings/keys ，添加SSH Key。点击New ssh key


2. id_rsa.pub内容关联 将C盘中的 .ssh文件夹中的id_rsa.pub 文件的内容（记事本打开）复制到，Title随机命名。

添加成功显示：

[![](/image-20240808105030384.png)](https://github.com/liuhanchang/tech_exp/blob/main/images/image-20240808105030384.png)

五、SourceTree 下载 git 项目
1. 复制你的 git 地址


2. 点击clone，将地址粘贴在路径中：

点击clone即可下载到source tree中。
