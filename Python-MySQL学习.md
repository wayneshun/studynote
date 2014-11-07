
MySQL 安装以及设置；

MySQLdb Python 安装以及设置；（用python控制MySQLdb）

mysql -uroot -p 进入mysql

quit exit 退出

create database XXXX default charset = utf8;  创建数据库

settings.py修改（APPS和DATABASE,注意mysql和sqlite3的区别)

models.py 修改

from django.db import models

class Employee(models.Model):
	name = models.CharField(max_length=20)


python manage.py syncdb



use XXXX(使用数据库)

show tables;

desc blog_employee(查看表)


