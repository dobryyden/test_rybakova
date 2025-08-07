# Проект "База ваканский"

![Postgres Version](https://img.shields.io/badge/postgres-15-blue) 

## 📚 Описание

Этот проект представляет собой базу данных для хранения информации о вакансиях в **PostgreSQL**. Он позволяет добавлять, обновлять, удалять и запрашивать вакансии с использованием SQL-запросов.

## 🚀 Установка

1. Убедитесь, что у вас установлен PostgreSQL 15 или выше.
2. Создайте новую базу данных:

    ```sql
    createdb job_db
    ```

3. Подключитесь к базе данных:

    ```sql
    psql job_db
    ```

## 💻 Использование

1. Создание таблицы вакансий:

    ```sql
    CREATE TABLE jobs (
    id SERIAL PRIMARY KEY,
    title VARCHAR(100) NOT NULL,
    company VARCHAR(100) NOT NULL,    
    salary INTEGER,
    is_active BOOLEAN); 
    ```

### Примеры запросов:

1. Вывод активных вакансий вакансии:

    ```sql
    SELECT * FROM jobs WHERE is_active = true; 
    ```

2. Добавление новой вакансии:

    ```sql
    INSERT INTO jobs (title, company, salary, is_active)
    VALUES ('Data Engineer', 'PnG', 120000, true);
    ```