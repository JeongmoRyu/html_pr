# django_variable_routing

## str, int 둘 다 넣어주기

ex) ——/음식/갯수

1. 프로젝트 my_pjt
2. urls.py

```python
from django.contrib import admin
from django.urls import path, include
from prices import views

urlpatterns = [
    path('admin/', admin.site.urls),
    path('price/', include('prices.urls')),

]
```

1. settings.py에 installed apps에 prices라는 앱을 추가해준다. 

1. prices라는 앱을 만들어준다.
2. prices/urls.py

```html
from django.urls import path
from prices import views

urlpatterns = [
    path('<str:name>/<int:count>', views.price)
]
```

1. prices/views.py

```python
from django.shortcuts import render

def price(request, name, count):

    product_price = {
        "후라이드치킨":15000,
        "양념치킨":17000,
        "오븐치킨":12000,
        "간장치킨":17000,
        "스페셜메뉴":20000,
        
    }

    if product_price.get(name):
        price = product_price.get(name) * count
    else:
        price = 0
    context = {
        'list':product_price.keys(),
        'name': name,
        'count': count,
        'price': price
    }

    return render(request, 'prices/price.html', context)
```

1. price.html을 만들어준다.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-GLhlTQ8iRABdZLl6O3oVMWSktQOp6b7In1Zl3/Jr59b6EGGoI1aFkw7cmDA6j6gD" crossorigin="anonymous">

  <title>Document</title>
</head>
<body>

  {% if name in list %}
  
    <h1> {{name}} {{count}}마리의 가격은 {{price}}원 입니다. </h1>

  {% else %}
    <h1> {{name}}은/는 저희 매장에 없습니다. </h1>
  {% endif %}

  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js" integrity="sha384-w76AqPfDkMBDXo30jS1Sgez6pr3x5MlQ1ZAGC+nuZB+EYdgRZgiwxhTBTkF7CXvN" crossorigin="anonymous"></script>
</body>
</html>
```

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/bfd3fbb6-802f-474d-b6ce-2283363f600a/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/92553318-0160-4129-8679-2ba2d354c619/Untitled.png)