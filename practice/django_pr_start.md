# django practice start

장고 연습 시작하기

```jsx
장고 시작하기

1. 인스톨하기
    - $ pip install diango==3.2.18
2. 프로젝트 생성
    - $ django-admin startproject my-pjt
3. 필요하다면 가상환경을 만들어준다.(프로젝트를 같이 진행하기 위해서 )
    - python -m venv venv
3-1. 가상환경 활성화
    - source venv/Scripts/activate
3-2. 가상환경 패키지 목록 저장
    - pip freeze > requirements.txt

4. APP를 만든다.
    - python manage.py startapp app

5. settings.py 의 installed_apps에 app을 넣어준다.

6. 서버를 실행한다.
    - python manage.py runserver

```

```jsx
from django.contrib import admin
from django.urls import path
from app import views

urlpatterns = [
    path('admin/', admin.site.urls),
    path('start/', views.start),
]
```