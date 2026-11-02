# API Overview

Нижче наведено демонстраційний API для To-Do App.

Базова адреса:

```text
https://api.todo-app.example/api
```

## GET /tasks

Повертає список завдань користувача.

### Запит

```http
GET /api/tasks
```

### Відповідь

```json
[
  {
    "id": 1,
    "title": "Виконати лабораторну роботу",
    "priority": "high",
    "completed": false
  }
]
```

## POST /tasks

Створює нове завдання.

### Запит

```http
POST /api/tasks
Content-Type: application/json
```

```json
{
  "title": "Підготувати презентацію",
  "priority": "medium"
}
```

### Відповідь

```json
{
  "id": 2,
  "title": "Підготувати презентацію",
  "priority": "medium",
  "completed": false
}
```

## GET /tasks/{id}

Повертає одне завдання за його ID.

### Запит

```http
GET /api/tasks/2
```

### Відповідь

```json
{
  "id": 2,
  "title": "Підготувати презентацію",
  "priority": "medium",
  "completed": false
}
```

## Коди відповіді

| Код | Значення |
|---|---|
| 200 | Успішний запит |
| 201 | Ресурс створено |
| 400 | Некоректний запит |
| 404 | Завдання не знайдено |
| 500 | Помилка сервера |
