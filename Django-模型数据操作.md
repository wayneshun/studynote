MySQL记录添加和查询的基本方法：

[Django 模型数据操作](http://study.163.com/course/courseLearn.htm?courseId=320022#/learn/video?lessonId=435044&courseId=320022)

python manage.py shell  启动shell



from blog.models import Employee #导入数据库


##插入数据的三种方法

###第一种方法

emp = Employee()                        #创建Emploeyee类的实例               
emp.name  =  'Allen'                     #修改字段赋值

emp.save()                                         #保存     

###第二种方法

emp = Employee(name = 'Wayne')  #实例化时直接修改字段属性

emp.save()

###第三种方法

Employee.objects.create(name = 'Kate')     #调用create方法直接修改

##查看数据库
	
use database
select * from blog_employee;

##查询：
emps = Employee.objects.all()    

emps          #输出

emps[0].name

修改models.py中的类，增加unicode方法

from django.db import models

class Employee(models.Model):
	name = models.CharField(max_length=20)

	def __unicode__(self):
		return self.name

##修改urls.py

增加 url(r'^index/$', 'blog.views.index'),


##修改blog下views.py:

from django.shortcuts import render
from django.shortcuts import render_to_response
from blog.models import Employee


def index(req):
	emps = Employee.objects.all()
	return render_to_response('index.html',{'emps':emps})


##建议index.html文件

导入数据库


<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<title>无标题文档</title>
</head>

<body>
{% for emp in emps %}
<div>{{ forloop.counter}} {{emp}}</div>
{% endfor %}
<div>共有{{emps.length}}记录</div>
</body>
</html>


















