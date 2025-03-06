# Spotify Clone Back-end

Этот проект представляет собой бэкенд для клона Spotify, разработанный с использованием современных технологий и инструментов. Основная цель проекта — предоставить API для управления пользователями, аутентификации и загрузки файлов (например, музыки).
## Contributors

[@user1](https://github.com/DKhorov)
[@user2](https://github.com/wiwokand)  



## Основные функции

- **Аутентификация пользователей**: Регистрация и вход с использованием JWT (JSON Web Tokens) для безопасной аутентификации.
- **Загрузка файлов**: Возможность загрузки музыкальных файлов на сервер с использованием `multer`.
- **Работа с базой данных**: Использование MongoDB для хранения данных пользователей и другой информации.

## Технологии

- **Node.js**: Среда выполнения JavaScript на стороне сервера.
- **Express.js**: Фреймворк для создания веб-приложений и API.
- **MongoDB**: NoSQL база данных для хранения данных.
- **Mongoose**: ODM (Object Data Modeling) библиотека для работы с MongoDB.
- **JWT (JSON Web Tokens)**: Используется для аутентификации и авторизации пользователей.
- **Bcrypt**: Библиотека для хеширования паролей.
- **Multer**: Middleware для обработки загрузки файлов.
- **CORS**: Middleware для обработки кросс-доменных запросов.

## Установка и запуск

1. **Клонирование репозитория**:
   ```bash
   git clone https://github.com/ваш-username/spotify-clone-backend.git
   cd spotify-clone-backend
   ```

2. **Установка зависимостей**:
   ```bash
   npm install
   ```

3. **Настройка базы данных**:
   - Убедитесь, что у вас установлен и запущен MongoDB.
   - Обновите строку подключения к MongoDB в файле `index.js`:
     ```javascript
     mongoose.connect('mongodb+srv://ваш-username:ваш-пароль@cluster0.rmyvs.mongodb.net/ваша-база-данных?retryWrites=true&w=majority&appName=Cluster0');
     ```

4. **Запуск сервера**:
   ```bash
   npm run start:dev
   ```
   Сервер будет запущен на порту 4000.

## API Endpoints

- **POST /auth/register**: Регистрация нового пользователя.
  - Тело запроса:
    ```json
    {
      "email": "user@example.com",
      "fullName": "John Doe",
      "password": "password123",
      "avatarUrl": "http://example.com/avatar.jpg"
    }
    ```

- **POST /auth/login**: Вход пользователя.
  - Тело запроса:
    ```json
    {
      "email": "user@example.com",
      "password": "password123"
    }
    ```

- **POST /upload**: Загрузка музыкального файла.
  - Формат запроса: `multipart/form-data`
  - Поле: `music` (файл)

## Структура проекта

- **index.js**: Основной файл сервера, содержащий настройки и маршруты.
- **package.json**: Файл с зависимостями и скриптами для запуска проекта.
- **control.js**: Контроллеры для обработки запросов на регистрацию и вход.
- **user.js**: Модель пользователя для MongoDB.



Это первая версия Back-end 
