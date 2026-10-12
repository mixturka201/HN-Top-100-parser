# Hacker News Top 100 Parser

Парсер топ-100 новостей с [Hacker News](https://news.ycombinator.com) через официальный API

## Описание

- Получает список топ-новостей через API
- Собирает данные: заголовок, автор, рейтинг, комментарии, дата, ссылка
- Сортирует по рейтингу
- Сохраняет в Excel с кликабельными ссылками

## Установка

```bash
pip install -r requirements.txt
```

## Запуск

```bash
python hn_parser.py
```

Результат - файл 'hn_top100.xlsx'

## Технологии

- Python 3.8+
- `requests` — HTTP-запросы к API
- `openpyxl` — запись в Excel

## API

Используется публичный API Hacker News: https://github.com/HackerNews/API

Без авторизации, без ключей.