# API Yatube Project
API для Yatube
# Технологии
Python 3.7.9
Django 2.2.19
# Описание
***API Yatube для взаимодействия с другими программами***
### Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone git@github.com:ErnestAbuz/api_final_yatube.git
```
```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv env
```

- Для Linux:

```
source env/bin/activate
```

- Для Windows:

```
source env/Scripts/activate
```

Установить зависимости из файла requirements.txt:

```
python3 -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python3 manage.py migrate
```

Запустить проект:

```
python3 manage.py runserver
```

Примеры запросов:

- Получение списка доступных сообществ.

- Запрос:
```
GET http://127.0.0.1:8000/api/v1/groups/
```

- Ответ:

```
[
  {
    "id": 0,
    "title": "string",
    "slug": "string",
    "description": "string"
  }
]
```

- Добавление нового комментария к публикации.

- Запрос:

```
POST http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/
```

```
{
"text": "Ваш текст"
}
```

- Ответ:

```
{
"id": 1,
"author": "author",
"text": "Ваш текст",
"created": "2022-07-24T17:15:00Z",
"post": 1
}
```
# Автор
Эрнест
