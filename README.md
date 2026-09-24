# LMS — 30.1 Вьюсеты и дженерики

Бэкенд LMS-системы на Django REST Framework: курсы и уроки, CRUD через ViewSet и Generic-классы.

## Стек

- Python, Django 5.2
- Django REST Framework
- SQLite

## Приложения

- `users` — кастомная модель пользователя (авторизация по email, телефон, город, аватар)
- `lms` — модели «Курс» и «Урок» (связь один-ко-многим)

## Установка и запуск

```
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

## Эндпоинты

Курсы (ViewSet + DefaultRouter):

- `GET/POST /courses/`
- `GET/PUT/PATCH/DELETE /courses/<id>/`

Уроки (Generic-классы):

- `GET/POST /lessons/`
- `GET/PUT/PATCH/DELETE /lessons/<id>/`

Профиль пользователя (доп. задание, ViewSet):

- `GET/POST /users/`, `GET/PUT/PATCH/DELETE /users/<id>/`

Все эндпоинты возвращают JSON и проверяются через Postman. Авторизация не настраивается
(разрешение `AllowAny`) — согласно заданию.
