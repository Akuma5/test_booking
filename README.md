# README.md

## 🏢 Booking API — Система бронирования переговорных комнат


## 🚀 Быстрый старт

### 🔧 Клонирование и запуск проекта
```bash
git clone https://github.com/your-username/booking-api.git
cd booking-api
cp .env.example .env
docker-compose up --build
```

Проект будет доступен на `http://localhost:8000/`

### ⚙️ Миграции и суперпользователь
```bash
docker-compose exec web python manage.py migrate
docker-compose exec web python manage.py createsuperuser
```

---

## 🔑 Аутентификация
- `POST /api/token/` — получение токена
- `POST /api/token/refresh/` — обновление токена

Пример тела запроса:
```json
{
  "username": "admin",
  "password": "yourpassword"
}
```

---



## 🧪 Тестирование
```bash
docker-compose exec web pytest
```
или (если используешь стандартные Django тесты):
```bash
docker-compose exec web python manage.py test
```
