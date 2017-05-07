# CentOS 7下MySQL 5.7安装 #
本文描述的安装是采用通用的二进制压缩包（linux - Generic）以解压方式安装<br/>

Step1 :下载通用安装二进制包<br/>
ps:CentOS 7的yum源中貌似没有正常安装mysql时的mysql-sever文件 ->需要去官网上下载<br>

<code> wget http://dev.mysql.com/get/mysql-community-release-el7-5.noarch.rpm  </code><br>

<code>rpm -ivh mysql-community-release-el7-5.noarch.rpm </code><br>

<code> yum install mysql-community-server</code><br>

初次登录mysql  在命令行输入MYSQL<br>
<code>mysql</code><br>

设置MYSQL密码
<code>mysql -uroot - p </code><br>

创建数据库
<code>create database h_test;  </code><br>     

查看数据库
<code>show databases;  </code><br>

查看数据库信息    
<code>show create database h_test;</code><br>

修改数据库的编码，可使用上一条语句查看是否修改成功<br>
<code>alter database h_test default character set gbk collate gbk_bin;   </code><br>   

删除数据库

<code>drop database h_test;</code><br>

# 表的约束 #

<table>
<thead>
<tr>
<th style="text-align:left">约束条件</th>
<th style="text-align:center">说明</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left">PRIMARY KEY</td>
<td style="text-align:center">主键约束，用于唯一标识对应的记录</td>
</tr>
<tr>
<td style="text-align:left">FOREIGN KEY</td>
<td style="text-align:center">外键约束</td>
</tr>
<tr>
<td style="text-align:left">NOT NULL</td>
<td style="text-align:center">非空约束</td>
</tr>
<tr>
<td style="text-align:left">UNIQUE</td>
<td style="text-align:center">唯一性约束</td>
</tr>
<tr>
<td style="text-align:left">DEFAULT</td>
<td style="text-align:center">默认值约束，用于设置字段的默认值</td>
</tr>
</tbody>
</table>









