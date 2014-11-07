##time模块方法：
time.time():获取当前时间的时间戳

时间戳转换为北京时间：http://tool.chinaz.com/Tools/unixtime.aspx

time.localtime():接受一个时间戳，并把它转化为一个当前时间的元组。不给参数的话就会默认将time.time()作为参数传入

time.mktime():和time.localtime()相反，它把一个时间元组转换成时间戳（这个必须要给一个参数）

time.asctime():把一个时间元组表示为：“Sun Jul 28 03:35:26 2013”这种格式，不给参数的话就会默认将time.localtime()作为参数传入

time.ctime():把一个时间戳转换为time.asctime()的表达格式，不给参数的话就会默认将time.time()作为参数传入

time.gmtime():将一个时间戳转换为UTC+0时区（中国应该是+8时区，相差8个小时）的时间元组，不给参数的话就会默认将time.time()作为参数传入

time.strftime(format,time.localtime()):将一个时间元组转换为格式化的时间字符,不给时间元组参数的话就会默认将time.localtime()作为参数传入
例如web日志里面的时间格式就是time.strftime('%d/%b/%Y:%X')
返回结果：Sun Jul 28 04:37:38 2013

[参考资料](http://zeping.blog.51cto.com/6140112/1259083)

##日期模块：

[直接看这里吧](http://www.w3cschool.cc/python/python-date-time.html)
