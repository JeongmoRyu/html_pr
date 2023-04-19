# django make freetalk

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5c934af4-7248-4b66-89ac-928a218b82a7/Untitled.png)

- articles/templates/articles/create.html

```html
{% extends 'base.html' %}

{% block content %}
	<h1 class='text-center'>성공적으로 글이 작성되었습니다.</h1>
	<a href="{% url 'articles:index' %}">index</a>
{% endblock content %}
```

- articles/templates/articles/detail.html

```html
{% extends 'base.html' %}

{% block content %}
  <h1 class="text-center">Detail</h1>
  <h2>작성자 : {{article.title}} </h2>

  <hr>
  <p>글 내용 : {{article.content}} </p>
  <p>글 생성시각: {{article.created_at}} </p>
  <p>글 수정시각: {{article.created_at}} </p>
	<a href=" {% url 'articles:index' %} ">목록보기</a>
  <a href="{% url 'articles:update' article.pk %}">수정하기</a>
<form action="{% url 'articles:delete' article.pk %}">
  {% csrf_token %}
  <input type="submit" value="삭제하기" />
<hr>
  <a href=" ">이전</a>
  <a href=" ">이후</a>
</form>
{% endblock content %}
```

- articles/templates/articles/index.html

```html
{% extends 'base.html' %}

{% block content %}
  <h1 class=text-center>게시판</h1>
  <a href="{% url 'articles:new' %}">잡담하기</a>
  <hr>
  {% for article in articles %}
    <p>글 번호: {{ article.pk }}</p>
    <p>
      <a href="{% url 'articles:detail' article.pk %}"
        >글 제목 : {{article.title}}</a
      >
    </p>
    <p>글 내용: {{ article.content }}</p>
    <a href="{% url 'articles:update' article.pk %}">수정하기</a>
    <form action="{% url 'articles:delete' article.pk %}">
      {% csrf_token %}
      <input type="submit" value="삭제하기" />
    </form>
    <hr>     
  {% endfor %}
{% endblock content %}
```

- articles/templates/articles/new.html

```html
{% extends 'base.html' %}

{% block content %}
  <h1 class='text-center'> NEW</h1>

  <hr>
  <form action="{% url 'articles:create' %}" method="POST">
    {% csrf_token %}
    <label for="title">작성자: </label>
    <input type="text" name="title"><br>
    <label for="content">내용: </label>
    <textarea name="content" cols="30" rows="5"></textarea><br>
    <input type="submit">
  </form>
  <hr>
  <a href="{% url 'articles:index'%}">[back]</a>
{% endblock content %}
```

- articles/templates/articles/update.html

```html
{% extends 'base.html' %}

{% block content %}
  <h1>UPDATE</h1>
  <hr>

  <form action="{% url 'articles:update' article.pk %}" method="POST">
    {% csrf_token %}
    {{ form.as_p }}
    <input type="submit">
  </form>

  <hr>
  <a href="{% url 'articles:detail' article.pk %}">[BACK]</a>
{% endblock content %}
```

- articles/forms.py
- 

```python
from django import forms
from .models import Article

class ArticleForm(forms.ModelForm):
    class Meta:
        model = Article
        fields = '__all__'
```

- articles/models.py

```python
from django.db import models

class Article(models.Model):
    title = models.CharField(max_length=10)
    content = models.TextField()
    created_at = models.DateTimeField(auto_now_add=True)
    updated_at = models.DateTimeField(auto_now=True)

    def __str__(self):
        return f'{self.id}번째글 - {self.title}'
```

- articles/urls.py

```python
from django.urls import path
from . import views

app_name='articles'

urlpatterns = [
    path('',views.index,name='index'),
    path('new/',views.new,name='new'),
    path('<int:pk>/', views.detail, name='detail'),
    path('create/', views.create, name='create'),
    path('<int:pk>/delete/', views.delete, name='delete'),
    path('<int:pk>/update/', views.update, name='update'),
]
```

- articles/views.py

```python
from django.shortcuts import render, redirect
from .models import Article
from .forms import ArticleForm

def index(request):
    articles = Article.objects.all()
    context = {
        'articles': articles,
    }
    return render(request, 'articles/index.html', context)

def detail(request, pk):
    article = Article.objects.get(pk=pk)
    context = {'article': article}
    return render(request, 'articles/detail.html', context)

def new(request):
    return render(request,'articles/new.html')

def create(request):
    if request.method == 'POST':
        form = ArticleForm(request.POST)
        if form.is_valid():
            article = form.save()
            return redirect('articles:detail', article.pk)
    else:
        form = ArticleForm()

    context = {'form': form }
    return render(request, 'articles/create.html', context)

def delete(request, pk):
    article = Article.objects.get(pk=pk)
    article.delete()
    return redirect('articles:index')

def update(request, pk):
    article = Article.objects.get(pk=pk)
    if request.method == 'POST':
        form = ArticleForm(request.POST, instance=article)
        if form.is_valid():
            form.save()
            return redirect('articles:detail', article.pk)
    else:
        form = ArticleForm(instance=article)
        
    context = {'form': form, 'article': article}
    return render(request, 'articles/update.html', context)
```

- project4/urls.py

```python
from django.contrib import admin
from django.urls import path, include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('articles/', include('articles.urls'))
]
```

- templates/base.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Project4</title>
</head>
<body>
  {% block content %}
  {% endblock %}
</body>
</html>
```

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e55266ef-3a9d-472d-b195-26f21e35c06c/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/55d895d5-5c59-467e-94b0-7b673779a719/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f36e72b7-5a49-4c4a-8a32-546a31bf0444/Untitled.png)