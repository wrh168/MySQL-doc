# 安装MySQL

方法/步骤
 

    1

    查找以前是否安装有mysql，使用下面命令：

    rpm -qa|grep -i mysql

    如果显示有如下包则说明已安装mysql
    
    2

    下载mysql的rpm包

    3

    下载后放到Liunx服务器中
    
    输入ll
    
    4

    安装MySQL Server的rpm包

    rpm -ivh MySQL-server-5.6.21-1.linux_glibc2.5.x86_64.rpm

    安装完成后会生成root用户的随机密码，请使用“cat /root/.mysql_secret”或类似命令进行查看。

    5
    
    安装MySQL客户端

    rpm -ivh MySQL-client-5.6.21-1.linux_glibc2.5.x86_64.rpm

    6
    
    安装MySQL开发依赖包

    rpm -ivh MySQL-devel-5.6.21-1.linux_glibc2.5.x86_64.rpm

    7
    
    启动msyql

    如下命令启动MySQL：

    service mysql start

    可使用SET PASSWORD命令修改root用户的密码，参考如下：SET PASSWORD = PASSWORD('root123456');
    
    8

    登录MySQL

    使用mysql命令登录MySQL服务器，运行MySQL的命令时，会提示需要设置root用户密码

    9

    安装成功
   
