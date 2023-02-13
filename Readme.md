# GoHFLabsParcer

- [GoHFLabsParcer](#gohflabsparcer)
  - [Описание](#описание)
  - [Инструкция по применению](#инструкция-по-применению)
  - [Сборка](#сборка)
  - [Структура проекта](#структура-проекта)
  - [Разработчики](#разработчики)

## Описание
По техническому задания требовалось написать скрипт для парсинга таблицы с [сайта](https://confluence.hflabs.ru/pages/viewpage.action?pageId=1181220999).

Я обнаружил API EndPoint позволяющий избежать прямого поиска нужных dom элементов в html коде.

[Ссылка на документ с результатом](https://docs.google.com/document/d/1ceHYcsZc3RGTz0X5zXY2vDdWeQXR3wiLWDhdPcD50XI/edit?usp=sharing)

## Инструкция по применению

- Для работы требуется иметь сервисный аккаунт в google cloud. 

*P.S: В конфиг файле, находится актуальные данные сервисного профиля, можете запустить и проверить. Не за что :)*

- Выставить переодичность выполнения можно в конфигурационной файле поле с именем "time_to_repeat", время указывается в минутах. (Стандартное время повторений 5 минут).

Более подробнее можно прочитать в файле **Info.md** лежащим в директории **/config/Info.md**.

## Сборка
**Сборка через docker:**
- docker-compose up --build
    
**Сборка без docker:**
- go build ./cmd/app/main.go (В этом случе потребуется переместить **config.json** в **/cmd/app**)

## Структура проекта
``` 
.
├── app
│   └── cmd
│       └── main.go
├── config
│   ├── config.go
│   ├── goparcer-995b1e7e5b99.json
│   └── Info.md
├── Dockerfile
├── go.mod
├── go.sum
├── internal
│   ├── app
│   │   └── run.go
│   ├── entity
│   │   └── hflabs.go
│   └── usecase
│       ├── gdoc.go
│       └── hflabs.go
└── Readme.md

```
  
## Разработчики

- [OneByteForLife](https://github.com/OneByteForLife)
