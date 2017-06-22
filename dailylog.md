## 工作日志

#### 2017-6-16  星期五
    
   * 上午
   
        1.建立STU数据库
	
        2.建立information,course,school,score
   
   * 下午
   
        1.数据库表信息的增删改查
	
   
        
#### 2017-6-19  星期一
    
   * 上午
   
        1.安装atom
	
        2.配置atom
	
        3.下载CGI-STU
	
        4.拷贝到atom
   
    
    * 下午
    
        1.安装Apache
	
        2.Apache开启CGI
	
        3.修改目录权限
	
```linux
        sudo mkdir /usr/lib/cgi-bin/sx
        sudo chmod 777 /usr/lib/cgi-bin/sx
```	 
        4.设置Makefile

```linux
	vim Makefile
       	install:	 
	       	cp *.cgi /usr/lib/cgi-bin/sx
```		
        5.连接到网页
```linux
           localhost
```
        
#### 2017-6-20  星期二
    
  * 上午
   
   	
	1.将创建好的数据库表与网页进行连接
	
	2.通过调试实现学生信息管理系统的增删改查
	
	
   * 下午

	1.写课程设计实验报告
	
	2.进一步增加多页面功能
	
	
		
#### 2017-6-21  星期三

	
   * 上午
     
   	1.页面与数据库连接出现错误，进行代码调试
	
   * 下午
   
   	1.在页面或本地对代码、文件进行修改一定要及时上传，否则会出现更新不同步的问题
	
#### 2017-6-22 星期四


   * 上午
   
   
   	1.增加了假删除和还原效果
	
	2.关联四个表，实现彼此的连接和调用
	
	
   *  下午
    
    	1.完善文档中~
    
    
    

    
 

