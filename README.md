# Практическая работа 1
Голубев Илья ЭФМО-02-25
# Описание проекта
Минимальный HTTP-сервис на Go с использованием net/http и внешней зависимостью для генерации UUID
Цель: Развернуть рабочее окружение Go на Windows, создать минимальный HTTP-сервис на net/http, подключить и использовать внешнюю зависимость, собрать и проверить приложение.
Задачи: Установить Go и Git, проверить версии. Инициализировать модуль Go в новом проекте. Реализовать HTTP-сервер с маршрутами /hello (текст) и /user (JSON). Подключить внешнюю библиотеку (генерация UUID) и использовать её в /user. Запустить и проверить ответы curl/браузером. Собрать бинарник .exe и подготовить README и отчёт.
# Требования
Go версии 1.21 и выше
# Установка и запуск
Версии GO и Git

<img width="606" height="219" alt="GoGitVersion" src="https://github.com/user-attachments/assets/d7f9d514-ea4f-406d-8ec6-efb65616b451" />

Клонировать репозиторий:
```
git clone https://github.com/iliaglbv/PR1
cd helloapi
```
Команда запуска сервера:
```
go run ./cmd/server
```
# Структура проекта
```plaintext
helloapi/                # Корень проекта
├── cmd/                 # Основные исполняемые файлы
│   └── server/          # Сервер приложения
│       └── main.go      # Точка входа
├── go.mod               # Файл зависимостей Go
├── go.sum               # Контрольные суммы зависимостей
└── helloapi.exe         # Скомпилированный исполняемый файл (Windows)
```
# Основные эндпоинты
Простой текстовый ответ

    curl http://localhost:8080/hello

Информация о пользователе (UUID и имя)

    curl http://localhost:8080/user

Проверка состояния сервиса

    curl http://localhost:8080/health

Примеры запросов
hello

<img width="863" height="495" alt="Hello_1" src="https://github.com/user-attachments/assets/70bcd01c-ea88-4527-b675-8823d08ba38d" />

user

<img width="865" height="428" alt="usert_1" src="https://github.com/user-attachments/assets/d62fe6ab-b941-4d77-b410-06ac331c810f" />

health

<img width="861" height="428" alt="healtht_1" src="https://github.com/user-attachments/assets/0ead581d-c0a2-4141-8a50-c9024fd37b09" />

# Порт по умолчанию 8080
Для смены порта установите переменную окружения

    $env:APP_PORT="8081"

В кавычках меняется порт


