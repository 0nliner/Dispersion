![Frame 2(1)](https://github.com/user-attachments/assets/4356dc2a-b911-4d42-825a-da288d5f9bb9)
# Dispersion API Gateway (Pre-alpha)

 
Собирайте, объединяйте и автоматизируйте API-интерфейсы 
🚀 Создавайте единые OpenAPI-спецификации из множества HTTP API

## Возможности
- **Простота использования** 
- **Динамическое объединение API** из разных систем
- **Генерация OpenAPI 3.1** в реальном времени
- **Маршрутизация** и перенаправление запросов
- **UI** для создания и настройки apigateway

## 🚀 Быстрый старт
1. Запуск через docker-compose
```
# docker-compose.yml
version: '3.8'

services:
  dispersion:
    build: .
    ports:
      - "8000:8000"
    volumes:
      - ./app:/app
    environment:
      - LOG_LEVEL=debug
    depends_on:
      - db

  db:
    image: postgresql:latest


  swagger:
    image: swaggerapi/swagger-ui
    ports:
      - "8080:8080"
    environment:
      SWAGGER_UI_URL: http://dispersion:8000/openapi.json
```
<hr>

## 🛠 Использование
На данный момент вся настройка apigateway производится через UI


## ROADMAP
- **Улучшение пользовательского опыта**
- **Логирование** интеграция с openobserve
- **Kubernetes** создание примера манифеста
- **Генерация клиентов** на Python/Typescript
- **Версионирование** возможность создавать разные версии спецификаций
- **Политики безопасности** (Bearer, API Key, OAuth)
- **Мониторинг** через Prometheus и Grafana
- **Транслитерация** добавление документации на английском языке
- **Кеширование** добавление механизма кеширования
