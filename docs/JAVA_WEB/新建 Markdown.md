# JAVA_WEB复习

## JDBC开发步骤

1. class.forname（"com.mysql.jdbc.Driver"）加载驱动
2. DriverManager.getConnection(url,name,password)创建数据库连接

​							JDBC：mysql：//IP地址：端口/，用户名，密码

3. connection。creatStatement				静态sql代码

    					   prepareStatement			动态sql代码	一般指带？的sql语句

   ​						CallableStatement

   4. Statement.executeQuery			查询更新记录

​						   executeUpdate				 增删改

​						   execute							  可查询可增删改

5. resultSet.next		从上往下的查询结果集
6. 释放数据库资源：调用close方法：java中通用规则：凡是实现了closeable接口的（即有close方法可调用）都可以释放资源

## JSP开发模式

Sun公司提供了两种开发模式：JSP Model1和JSP Model2

Model1：适用于小型WEB项目的快速开发

Model2：在Model1基础上提出，适用于多人合作的大型WEB项目开发

原始开发模式：

![JSP开发](C:/Users/26679/Desktop/JSP开发.png)

Model1：

![Model1](C:/Users/26679/Desktop/Model1.png)

MVC模式：

![MVC模式](C:/Users/26679/Desktop/MVC模式.png)

开发项目理念：高内聚低耦合

​						即将相同模块的代码尽可能的放置于一个模块中（高内聚），使模块与模块的功能间不相互干扰（低耦合）

​					：已确认功能无异的代码，不要自已造轮子

## 文件上传

1. 在WEB页面添加上传输入项

在页面中添加表单<form>,使用<input type="file">,<input type="text">,<input type="submit">

2. 在Servlet中读取上传文件的数据，并保存到本地硬盘中

借助于Commons-FileUpload组件中实现，



## 文件下载

无需组件直接使用Servlet类的输入输出，需要指定文件的路径，还需要在HTTP协议中设置两个消息头。

