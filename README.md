# Docker для PHP разработки
## Подходит для Laravel, Yii2, Codeigniter, Symfony, чистый PHP.
### При использовании фреймворка, очистить директорию "web".

Докер настроен с учетом модуля Xdebug.

Зависимости для чистого PHP:

```json

{
  "require-dev": {
    "symfony/var-dumper": "^6.3"
  }
}

```
, для использования функции dd();

```json

{
  "require": {
    "guzzlehttp/guzzle": "^7.8"
  }
}

```
, для работы с HTTP-клиентом и создания фейковфх данных API.

### Запуск и установка
- склонировать репозиторий;
- выполнить make start;

#### Доступные команды для make
##### composer:
- install
- validate

##### cocker-compose:
- up
- stop

##### up && install:
- start

##### test:
- test