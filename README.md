#### API_YaTube
### Проект позволяет обращаться к сервису YaTube просредством интерфейса Rest API
Данный проект позволит связывать приложения с сервисом YaTube. Что обеспечит доступ пользователя с разных платформ.

## Запуск проекта в dev-режиме

- Клонировать репозиторий и перейти в него в командной строке:
```
git clone https://github.com/nevladi/api_final_yatube.git 
cd api_final_yatube

```

- Cоздать и активировать виртуальное окружение:
```
    python3 -m venv env
    source venv/bin/activate
```
- Установить зависимости из файла requirements.txt
```
    python -m pip install --upgrade pip
    pip install -r requirements.txt
```
- Выполнить миграции:
```
    python manage.py migrate
```

- В папке с файлом manage.py выполнить команду:
```
    python manage.py runserver
```

В проекте есть такие эндпоинты
Получение и создание публикаций
/api/v1/posts/      методы: GET, POST
Получение отдельной публикации, ее редактирование
/api/v1/posts/{id}/    методы: GET, PUT, PATCH, DEL
Получение и создание комментариев к публикации
/api/v1/posts/{post_id}/comments/    методы: GET, POST
Получение и редактирование комментария к публикации
/api/v1/posts/{post_id}/comments/{id}/    методы: GET, PUT, PATCH, DEL
Получение списка сообществ
/api/v1/groups/     методы: GET
Получение информации о сообществе
/api/v1/groups/{id}/    метод: GET
Получение и создание подписок на авторов
/api/v1/follow/     методы: GET, POST
Получение JWT-токена
/api/v1/jwt/create/     метод: POST
Обновление JWT-токена
/api/v1/jwt/refresh/    метод: POST
Проверка JWT-токена
/api/v1/jwt/verify/     метод: POST
