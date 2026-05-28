# taski-docker

## Инструкция по установке

1. Клонируйте репозиторий:
   ```bash
   git clone https://github.com/kirill-9887/taski-docker
   cd ./taski-docker
   ```

2. Создайте файл окружения `.env` из шаблона:
   ```bash
   cp .env.example .env
   ```

3. Запустите проект через Docker:
   ```bash
   docker compose up -d --build
   ```

4. Настройка
   ```
   docker compose exec backend python manage.py collectstatic

   docker compose exec backend cp -r /app/collected_static/. /backend_static/static/

   docker compose exec backend python manage.py migrate
   ```

Проект будет доступен по адресу: `http://localhost:8000`
