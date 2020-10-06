[TOC]

### 1.安装
- centos7 下安装mysql5.7 
  - [mysql官网下载](https://www.mysql.com/)
  - wget https://dev.mysql.com/get/mysql57-community-release-el7-9.noarch.rpm
  - repo 安装  rpm -ivh mysql57-community-release-el7-9.noarch.rpm （执行完成后会在/etc/yum.repos.d/目录下生成两个repo文件mysql-community.repo mysql-community-source.repo）
  - 安装 yum install mysql-server
  - 启动 systemctl start mysqld
  - 获取密码 grep 'temporary password' /var/log/mysqld.log
  - mysql -uroot -pxx 
  - SET PASSWORD = PASSWORD('your new password') 修改密码
  -  flush privileges;
- 删除
  - 查看安装了那些东西 rpm -qa |grep -i mysql
  - 全部卸载 yum remove xxx
  - 查找mysql有关目录 find / -name mysql  并全部删除
  - 删除/etc/my.cnf  rm -rf /etc/my.cnf
  - 删除/var/log/mysqld.log rm -rf /var/log/mysqld.log
- 命令
  - systemctl status mysqld
  - systemctl start mysqld
  - systemctl stop mysqld
  - systemctl restart mysqld
  - vim /etc/my.cnf
  - 修改密码 alter  user 'root'@'localhost' identified by '#20as3SElksds0ew98'; 一定要加  flush privileges;
