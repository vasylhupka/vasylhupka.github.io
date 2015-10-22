---
published: true
layout: post
title: Сайт на Github
categories: Github
---



Mало кто знает, что Github кроме превосходного хостинга ваших Git проектов может также хостить ваш персональный сайт. Например на нем расположен этот блог. В своей первой статье я расскажу как максимально удобно настроить эту функциональность.

Для начала вам нужно быть зарегистрированным пользователем [Github](http://github.com/) и уметь работать с системой контроля версий [Git](http://git-scm.com/). Предположим вы готовы.

Первое, что вам потребуется — это создать на Github репозиторий с именем вида: _username.github.com_, где username ваш логин на сервисе. 

Вторым шагом мы создадим локальный репозиторий и привяжем его к удаленному:

{% highlight html %}
git init
echo 'Hello world!' > index.html
git add .
git commit -m 'Initial commit'
git remote add origin git@github.com:klen/klen.github.com.git
git push -u origin master
{% endhighlight %}

Отлично, ваш статический сайт уже готов! В течении 10 минут он появится по адресу: _username.github.com_. В дальнейшем он будет обновляться при коммитах в удаленный репозиторий.
