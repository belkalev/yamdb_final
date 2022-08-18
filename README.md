# yamdb_final

Проект http://130.193.41.54/api/v1/

![Yamdb_workflow](https://github.com/belkalev/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)

Проект YaMDb
========================================================
Проект YaMDb собирает отзывы пользователей на произведения.

### Запуск проекта

1. Склонировать проект и перейти в нужный репазиторий

`git clone git@github.com:belkalev/yamdb_final.git`
`cd infra`

2. Запустить сборку контейнера

`docker-compose up -d`

3. Выполнить миграции

`docker-compose exec web python manage.py migrate`

4. Собрать статику

`docker-compose exec web python manage.py collectstatic --no-input`

5. Заполнить БД из фикстур

`docker-compose exec web python manage.py loaddata fixtures.json`


### Файл  _.env_ :

`DB_ENGINE=django.db.backends.postgresql # указываем, что работаем с postgresql`
`DB_NAME=postgres # имя базы данных`
`POSTGRES_USER=postgres # логин для подключения к базе данных`
`POSTGRES_PASSWORD=postgres # пароль для подключения к БД (установите свой)`
`DB_HOST=db # название сервиса (контейнера)`
`DB_PORT=5432 # порт для подключения к БД`


Проект выполнен студентом курса Python-разработчик плюс Малявко  
                 Татьяной