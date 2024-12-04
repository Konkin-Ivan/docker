# Docker - контейнеры

## Готовая сборка для новых проектов

### Скачал, запустил, пользуешься

- в .env изменить ```PROJECT_NAME=base_docker```;
- в .gitignore добавить необходимые файлы и директории.

#### Используй команды из Makefile:

- make up - скачать образы контейнеров;
- make install - скачать зависимости для composer.json;
- make stop - остановить контейнеры.

Так же, можно использовать docker-compose: ```docker-compose exec php composer install``` аналог команды `make install`.

#### Для php

Отдельная сборка для php в директории Php.

#### Для Go

Отдельная директория для Golang в директории Golang.
