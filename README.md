# Docker-image
В директории What's behind this? представлено полное описание поставленной задачи проекта, тонкости реализации и условия выполнения.

Перед запуском нужно предварительно установить: Docker. Приведу вариант установки для MacOS через HomeBrew:

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)" - установка HomeBrew

brew cask install docker - установка Docker

Если возникла необходимость в альтернативном варианте установки:
Инструкция по установке Docker для всех платформ: https://docs.docker.com/desktop/

Сборку образа можно запустить командой docker build -t ЛюбоеИмя Путь, например: docker build -t Default .
Запуск контейнера docker run -p 443:443 -p 80:80 Default
В браузере:
127.0.0.1 - Индексация
127.0.0.1/wordpress - установка WordPress
127.0.0.1/phpmyadmin - вход в PhpMyAdmin (логин: hhanh, пароль: hhanh)
docker stop $(docker ps -q) - остановить все запущенные контейнеры
