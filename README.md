# Hacker News Top 100 Parser

![Daily HN Top 100](https://github.com/mixturka201/HN-Top-100-parser/actions/workflows/daily.yml/badge.svg)

Парсер топ-100 новостей с [Hacker News](https://news.ycombinator.com) через официальный API.

## Что делает

- Получает список топ-новостей через API
- Собирает данные: заголовок, автор, рейтинг, комментарии, дата, ссылка
- Сортирует по рейтингу
- Сохраняет в Excel с кликабельными ссылками
- Отправляет топ-5 новостей в Telegram ежедневно в 9:00 МСК

## Как это работает

1. GitHub Actions запускается по расписанию (каждый день в 6:00 UTC).
2. Парсер собирает топ-100 новостей через Hacker News API.
3. Сохраняет в Excel.
4. Отправляет топ-5 новостей в Telegram.

## Установка

```bash
pip install -r requirements.txt
```

## Запуск локально

1. Создай бота через `@BotFather` в Telegram.
2. Получи `chat_id` через `getUpdates`.
3. Создай `.env` в корне проекта:

```
TG_BOT_TOKEN=твой_токен
TG_CHAT_ID=твой_chat_id
```

4. Запусти:

```bash
python hn_parser.py
```

Результат — файл `hn_top100.xlsx` и сообщение в Telegram.

## Технологии

- Python 3.11
- `requests` — HTTP-запросы
- `openpyxl` — запись в Excel
- `python-dotenv` — хранение секретов
- Telegram Bot API
- GitHub Actions

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.