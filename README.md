# centos7ftp
  1安装vsftp

 <code> yum install -y vsftpd</code><br/>
  2设置开机启动

  <code> systemctl enable vsftpd</code><br/>
  3启动ftp服务

  <code> service vsftpd start</code><br/>
 
 4打开防火墙

 <code> firewall-cmd --zone=public --add-port=21/tcp --permanent</code><br/>
<code>  firewall-cmd --permanent --zone=public --add-service=ftp</code><br/>
 <code> firewall-cmd --reload</code><br/>
 
5.添加用户
<code> useradd -g root -d /home/data -s /sbin/nologin itsusername</code><br/>

6.设置用户密码
<code>passwd  itspassword

7.设置权限
<code>chown -R itsusername:root /home/data</code><br/>
<code>setsebool -P ftpd_full_access on</code><br/>

8.修改vsftp配置文件，禁用匿名登录
<code>vi /etc/vsftpd/vsftpd.conf</code><br/>
把：anonymous_enable=YES 改为： anonymous_enable=NO<br>
---> 按ESC键然后 输入  :wq  保存退出
