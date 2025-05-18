# Liquibase_HomeWork :green_book:
**Темы:**
- [entity](https://github.com/AbdulatipA/Liquibase_HomeWork/tree/master/src/main/java/org/example/liquibase_homework/entity)
- [table students](https://github.com/AbdulatipA/Liquibase_HomeWork/blob/master/src/main/resources/db/changelog/changes/001-create-student-table.yaml)
- [table courses](https://github.com/AbdulatipA/Liquibase_HomeWork/blob/master/src/main/resources/db/changelog/changes/002-create-course-table.yaml)
- [table students_and_courses](https://github.com/AbdulatipA/Liquibase_HomeWork/blob/master/src/main/resources/db/changelog/changes/003-create-student-and-course-table.yaml)




> Практическая задача: "Управление структурой БД через Liquibase"
> Цель задачи:
> Настроить миграции базы данных с помощью Liquibase в проекте на Spring Boot , чтобы управлять структурой базы данных через версионированные изменения.

Вы работаете над приложением для онлайн-обучения. В системе есть:
>Студенты (Student) и Курсы (Course) связь многие ко многим между студентом и курсом.
> Также нужно добавить логику подсчёта завершённых курсов и отслеживания прогресса.

>1. Создать таблицу student
>id (BIGINT, PK)
>full_name (VARCHAR(255), NOT NULL)
>email (VARCHAR(255), UNIQUE, NOT NULL)
>Добавить индекс для поля email. 

>2. Создать таблицу course
>id (BIGINT, PK)
>title (VARCHAR(255), NOT NULL)
>description (TEXT)
>duration_days (INT, DEFAULT 30)
>Добавить уникальный индекс на поле title.

>Создать таблицу  (связь многие ко многим)
>student_id (BIGINT, FK на student.id)
>course_id (BIGINT, FK на course.id)
>enrolled_at (DATETIME, DEFAULT CURRENT_TIMESTAMP)
>Установить составной первичный ключ из (student_id, course_id). 


