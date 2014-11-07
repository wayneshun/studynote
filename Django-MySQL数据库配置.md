###新建项目：
django-admin.py startproject XXXX
###新建应用：
django-admin.py startapp XXX
###在新建项目中配置settings.py：

数据库配置
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'wayne2',
        'USER': 'root',
        'PASSWORD': '1123581321',
        'HOST': '',
        'PORT': '',
    }
}

INSTALLED_APPS 配置：
增加应用项目，如应用为blog，则增加
‘blog',如下：

INSTALLED_APPS = (
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'blog',
)
