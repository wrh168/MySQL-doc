# 学生信息管理系统

### 数据库设计

#### 学校表（school）

|   字段名   |	  数据类型   |	  字段限制   |  	描述   |
|-----------|-------------|--------------|-----------|
|school_id	|  varchar(20)|	 primary key |	学校编号  |
|school_name|	 varchar(50)|	   not null  |  学校名称  |
|school_addr|	varchar(255)|  	 not null	 |  学校地址  |
|school_tel	|  varchar(20)|   not null	 |  学校电话  |

#### 学生表（information）

|   字段名   |	  数据类型   |	  字段限制   |  	描述   |
|-----------|-------------|--------------|-----------|
|studentNo  |  varchar(10)|  primary key |  	学号   |
|studentName|	 varchar(30)|	  not null	 |    姓名   |
|sex	      |  varchar(10)|   not null	 |    性别   |
|birthday	  |  datetime	  |   not null	 |   出生日期 |
|school_id	|  varchar(20)|		           |   学校编号 |

#### 课程表（course）

|   字段名   |	  数据类型   |	  字段限制   |  	描述   |
|-----------|-------------|--------------|-----------|
|courseNo	  |  varchar(10)|  	primary key|   课程号  |
|courseName	|  varchar(30)|	   not null	 |   课程名  |
|creditHour	|  varchar(6)	|    not null  |   	学分   |
|priorCourse|	 varchar(30)|    not null	 |   选修课程 |


#### 成绩表（score）

|   字段名   |	  数据类型   |	  字段限制   |  	描述   |
|-----------|-------------|--------------|-----------|
|studentNo	|  varchar(10)|	 primary key |	  学号   |
|courseNo	  |  varchar(10）| primary key |   课程号   |
|score     	|  varchar(10）| not null	  |    成绩    |


