Хорошо, давай обновлю README.md с четкой информацией о том, что нужно импортировать/установить:

---

## 📝 Обновленный README.md

```markdown
# Practice 4-6: Users Management App

Веб-приложение для управления пользователями с REST API и Swagger документацией.

## 📋 Описание

Приложение позволяет создавать, редактировать и удалять пользователей. Бэкенд предоставляет REST API с полной Swagger документацией.

## 🏗️ Структура проекта

```
practice4/
├── backend/           # Сервер на Express
│   ├── app.js         # Основной файл сервера с Swagger
│   ├── package.json   # Зависимости бэкенда
│   └── node_modules/
├── frontend/          # Клиент на React
│   ├── src/
│   │   ├── api/       # API клиент (axios)
│   │   ├── components/# React компоненты
│   │   └── pages/     # Страницы приложения
│   └── package.json   # Зависимости фронтенда
└── README.md
```

## 🚀 Технологии

| Компонент | Технология |
|-----------|------------|
| Backend | Node.js + Express |
| Frontend | React 18 |
| API | REST |
| Документация | Swagger (OpenAPI 3.0) |
| HTTP клиент | Axios |
| Генерация ID | nanoid |

## 📦 Установка и запуск

### ⚠️ ВАЖНО: Что нужно установить

#### **1. Backend зависимости:**

```bash
cd backend

# Основные зависимости (уже в package.json):
npm install express cors nanoid

# Для разработки (Swagger):
npm install -D swagger-jsdoc swagger-ui-express
```

#### **2. Frontend зависимости:**

```bash
cd frontend

# Основные зависимости (уже в package.json):
npm install react react-dom react-scripts
npm install axios
npm install sass
```

### 🔧 Запуск приложения

**Шаг 1: Запусти бэкенд**

```bash
cd backend
npm install          # Установи зависимости (первый раз)
node app.js          # Запусти сервер
```

✅ Сервер запустится на: **http://localhost:3000**  
✅ Swagger документация: **http://localhost:3000/api-docs**

**Шаг 2: Запусти фронтенд** (в другом терминале)

```bash
cd frontend
npm install          # Установи зависимости (первый раз)
npm run dev          # Запусти React приложение
```

✅ Приложение откроется на: **http://localhost:3001**

## 🔌 API Endpoints

| Метод | Endpoint | Описание |
|-------|----------|----------|
| GET | /api/users | Получить всех пользователей |
| GET | /api/users/:id | Получить пользователя по ID |
| POST | /api/users | Создать пользователя |
| PATCH | /api/users/:id | Обновить пользователя |
| DELETE | /api/users/:id | Удалить пользователя |

## 📝 Функционал

- ✅ Просмотр списка пользователей
- ✅ Создание нового пользователя
- ✅ Редактирование существующего
- ✅ Удаление пользователя
- ✅ Swagger документация API
- ✅ CORS настроен
- ✅ Логирование запросов

## 📚 Что импортировать в коде

### Backend (app.js):

```javascript
const express = require('express');
const cors = require('cors');
const { nanoid } = require('nanoid');
const swaggerJsdoc = require('swagger-jsdoc');
const swaggerUi = require('swagger-ui-express');
```

### Frontend (src/api/index.js):

```javascript
import axios from "axios";
```

### Frontend (компоненты):

```javascript
import React, { useEffect, useState } from "react";
import { api } from "../../api";
```

## 👨‍ Автор

Студент ИПТИП, 4 семестр, 2025/2026 уч. год

## 📚 Дисциплина

Фронтенд и бэкенд разработка
```

---

## 🎯 Главное, что нужно запомнить:

| Что | Где | Команда |
|-----|-----|---------|
| **Backend зависимости** | `backend/` | `npm install express cors nanoid swagger-jsdoc swagger-ui-express` |
| **Frontend зависимости** | `frontend/` | `npm install axios sass` |
| **Запустить бэкенд** | `backend/` | `node app.js` |
| **Запустить фронтенд** | `frontend/` | `npm run dev` |

Теперь в README четко указано, что и куда устанавливать! 🚀