# Используем официальный образ Clojure
FROM clojure:latest

# Устанавливаем необходимые пакеты
RUN apt-get update && \
    apt-get install -y \
        curl \
        git \
        rlwrap && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# Создаём пользователя с тем же UID/GID, что и на хосте
ARG USER_ID=1000
ARG GROUP_ID=1000
RUN groupadd -g ${GROUP_ID} clojure-user && \
    useradd -u ${USER_ID} -g clojure-user -m clojure-user
# Устанавливаем рабочую директорию
WORKDIR /usr/src/web/
# Меняем владельца рабочей директории
RUN chown -R clojure-user:clojure-user /usr/src/web
# Переключаемся на созданного пользователя
USER clojure-user

# Открываем порт для REPL
EXPOSE 5555

# Команда для запуска REPL с использованием Clojure CLI
CMD ["sh", "-c", "clojure -J-Dclojure.server.repl=\"{:port 5555 :accept clojure.core.server/repl}\" & tail -f /dev/null"]
