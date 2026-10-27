# Infra project

Учебный инфраструктурный репозиторий курса 

<!-- Допишите сюда -->
Учебный проект: настройка веб-сервера через Ansible и запуск в Docker.
Репозиторий проверен через веб-интерфейс GitHub

## Запуск в Docker

```bash
docker build -t infra-web:1.0 docker/
docker run -d --name infra-web -p 8080:80 infra-web:1.0
curl http://localhost:8080
docker rm -f infra-web
```
