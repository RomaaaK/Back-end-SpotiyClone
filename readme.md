# Spotify Clone Back-end

Этот проект представляет собой бэкенд для клона Spotify, разработанный с использованием современных технологий и инструментов. Основная цель проекта — предоставить API для управления пользователями, аутентификации и загрузки файлов (например, музыки).
## Contributors

[@user1](https://github.com/DKhorov)
[@user2](https://github.com/wiwokand)  




## Технологии

- **Node.js**: Среда выполнения JavaScript на стороне сервера.
- **Fastify**: Фреймворк для создания веб-приложений и API.
- **PostgreSQL**: SQL база данных для хранения данных.
- **Redis**: NoSQL база данных для работы с временными даннными.
- **Prisma**: ORM библиотека для работы с PostgreSQL.
- **JWT (JSON Web Tokens)**: Используется для аутентификации и авторизации пользователей.
- **Bcrypt**: Библиотека для хеширования паролей.

## Установка и запуск

1. **Клонирование репозитория**:
   ```bash
   git clone https://github.com/DKhorov/Back-end-SpotiyClone
   cd Back-end-SpotiyClone
   git switch -c branch_name
   ```

2. **Установка зависимостей**:
   ```bash
   npm install
   ```

3. **Настройка базы данных**:
   - Убедитесь, что у вас установлен и запущен PostgreSQL.
   - Убедитесь, что у вас установлен и запущен Redis.
   - Создайте `.env` файл и заполните файл по примеру из файла `.env.example`
   - Произведите генерацию ORM командой `npm run db:gen`
   - Произведите миграцию ORM командой `npm run db:migrate dev -- --name init`

4. **Запуск сервера**:
   ```bash
   npm run run:dev
   ```

## API Endpoints

API Endpoints можно посмотреть по ссылке http://localhost:{port}/docs при запуске проекта.