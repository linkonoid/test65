### Задача: реализовать следующий функционал на свое усмотрение
 
- Создать проект на PHP.
- Создать таблицу и модель с полями, охватывающими столбцы из CSV файла.
-Принимать и парсить этот файл в созданную модель одним из способов:
    1. Используя страницу с формой для загрузки файла
    2. Используя апи метод принимающий файл
- Сохранить эти записи в базу в созданную таблицу
- Вывести на отдельную страницу список выгруженных данных
- Разместить результат работ на любом хостинге, прислать ссылку.

### Реализация

По времени реализация заняла порядка 6 часов на непосредственное кодирование и несколько часов на проработку архитектурных решений, настройку окружения и отлов ошибок парсинга "кривого" тестового .csv 

Что имеем по структуре проекта:
- "под капотом" реализован полноценный роутер для маршрутизации запросов (например, выдаётся 404 ошибка при отсутствующем в конфигурации роуте) 
- конфигурационный файл в .yaml формате, где определяем роуты, модели данных (пока это реализовано в рамках модели данных тестового .csv) и прочие настройки
- [Twig](https://twig.symfony.com/)  для реализацие view-ов с использованием шаблонов (в конфиге можно включить кэширование)
- структура проекта максимальна проста и напоминает Laravel и подобные фреймворки с входной точкой index.php и автоматическим подключением composer-библиотек и нативных классов.
