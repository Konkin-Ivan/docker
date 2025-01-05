# Используем официальный образ Clojure с поддержкой Leiningen
FROM clojure:latest

RUN apt-get update && apt-get install -y \
    curl \
    git \
    && rm -rf /var/lib/apt/lists/*

# Создаём пользователя с тем же UID/GID, что и на хосте
ARG USER_ID=1000
ARG GROUP_ID=1000
RUN groupadd -g ${GROUP_ID} clojure-user && \
    useradd -u ${USER_ID} -g clojure-user -m clojure-user

# Устанавливаем рабочую директорию
WORKDIR /usr/src/web/app/

# Меняем владельца рабочей директории
RUN chown -R clojure-user:clojure-user /usr/src/web

# Переключаемся на созданного пользователя
USER clojure-user

# Открываем порт для REPL
EXPOSE 5555

# Команда для запуска REPL и поддержания контейнера в активном состоянии
CMD ["sh", "-c", "lein repl :headless :host 0.0.0.0 :port 5555 & tail -f /dev/null"]
