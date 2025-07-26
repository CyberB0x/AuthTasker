# 📝 AuthTasker — To-Do API с авторизацией на Django REST Framework

**AuthTasker** — это простой, но функциональный REST API для управления задачами. Поддерживает регистрацию, аутентификацию по токену и полные CRUD-операции. Отлично подходит как демонстрация навыков Fullstack Python-разработчика.

---

## 🚀 Функциональность

- 🔐 Аутентификация по токену (`TokenAuthentication`)
- 🧾 CRUD для задач (создание, чтение, обновление, удаление)
- 🧑‍💼 Привязка задач к пользователю
- 📄 Документация Swagger/OpenAPI
- 📦 SQLite/PostgreSQL (по выбору)
- 📂 Готово к Docker'изации (опционально)

---

## 📁 Стек технологий

- [Django](https://www.djangoproject.com/)
- [Django REST Framework](https://www.django-rest-framework.org/)
- [drf-yasg](https://github.com/axnsan12/drf-yasg) — Swagger UI
- SQLite (по умолчанию)

---

## ⚙️ Установка и запуск

```bash
    # 1. Клонировать репозиторий
    git clone https://github.com/your-username/authtasker.git
    cd authtasker
    
    # 2. Создать виртуальное окружение
    python -m venv venv
    source venv/bin/activate  # Windows: venv\Scripts\activate
    
    # 3. Установить зависимости
    pip install -r requirements.txt
    
    # 4. Применить миграции и создать суперпользователя
    python manage.py migrate
    python manage.py createsuperuser
    
    # 5. Запустить сервер
    python manage.py runserver
```
# 🔑 Получение токена
```commandline
    POST /api-token-auth/
    Content-Type: application/json
    
    {
      "username": "your_username",
      "password": "your_password"
    }

```
# Используйте в заголовках:
* Authorization: Token ваш_токен 

# 🔗 API Endpoints
```commandline
    | Метод  | Endpoint           | Описание              |
    | ------ | ------------------ | --------------------- |
    | GET    | `/api/tasks/`      | Получить список задач |
    | POST   | `/api/tasks/`      | Создать новую задачу  |
    | PUT    | `/api/tasks/<id>/` | Обновить задачу       |
    | DELETE | `/api/tasks/<id>/` | Удалить задачу        |

```
# 🧪 Документация Swagger
```bash
   http://localhost:8000/swagger/ 
```

🤝 Поддержка
Если проект был полезен — поставьте ⭐ 