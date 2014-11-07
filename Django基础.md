
cd c:/
django-admin.py startproject XXXX
cd XXXX
django-admin.py startapp XXX
cd XXX
mkdir templates

settings.py
add 'XXX',

urls.py

url(r'^index/$','XXX.views.index'),  以index为url后缀

XXX/viesw.py

from django.shortcuts import render
from django.template import loader,Context,Template
from django.http import HttpResponse
from django.shortcuts import render_to_response


def index(req):
	t = loader.get_template('hello.html')
	c = Context({'uname':'wayne'})
	return HttpResponse(t.render(c))


def index1(req):
	t = Template('<h1>hello {{uname}}</h1>')
	c = Context({'uname':'wayne'})
	return HttpResponse(t.render(c))

def index2(req):
	return render_to_response('hello.html',{'uname':'wayne'})

cd XXXX

python manage.py runserver
