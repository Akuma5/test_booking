# README.md

## 🏢 Booking API — Система бронирования переговорных комнат

### 📦 Стек технологий
- Python 3.11
- Django 4.x
- Django REST Framework
- PostgreSQL
- JWT (SimpleJWT)
- Docker + docker-compose
- Swagger / ReDoc документация

---

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

## 📚 Документация
- Swagger: [http://localhost:8000/swagger/](http://localhost:8000/swagger/)
- ReDoc: [http://localhost:8000/redoc/](http://localhost:8000/redoc/)

---

## 🧪 Тестирование
```bash
docker-compose exec web pytest
```
или (если используешь стандартные Django тесты):
```bash
docker-compose exec web python manage.py test
```

---

## 📁 Структура проекта
- `booking/` — приложение бронирования
- `users/` — кастомная модель пользователя (если расширяется)
- `api/` — сериализаторы, viewsets, permissions
- `docker/` — файлы Docker

---

## 📌 Примечания
- Админ может создавать и редактировать переговорки
- Пользователь может бронировать только свободные слоты
- Проверка пересечений по времени и по пользователю встроена

---

> Автор: [Твое имя] — 2025
