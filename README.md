# Client Records Telegram Bot

Бот для записи клиентов и предоставления информации о продуктах и услугах барбершопа.

---

## 📋 Функционал приложения

- Отправка сообщений с фото, кнопками и ссылками.
- Интерактивное меню с переходами между разделами.
- Возможность записи через веб-приложение YClients.
- Просмотр продукции для бритья с возможностью вернуться в главное меню.
- Быстрый доступ к отзывам, Instagram, VK и маршруту до барбершопа.

---

## 🛠️ Технологии

- **Python**
- **FastAPI**
- **Python Telegram Bot** (версия 20.5)
- **Vercel** (для маршрутизации)
- **Uvicorn** (для запуска FastAPI)

---

## 📂 Структура приложения

client-records-telegram-bot/ ├── api/ │ └── index.py # Основной файл с кодом бота ├── venv/ # Виртуальное окружение (не добавляйте в Git) ├── .gitignore # Исключение виртуального окружения из репозитория ├── requirements.txt # Зависимости проекта ├── vercel.json # Конфигурация Vercel для маршрутизации ├── README.md # Документация для проекта (опционально) └── .env # Переменные окружения (не для публичного репозитория)


## 🚀 Установка и настройка

### 1. Клонируйте репозиторий

```bash
git clone https://github.com/your-username/client-records-telegram-bot.git
cd client-records-telegram-bot
```

### 2. Установите виртуальное окружение и зависимости

```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

📦 Установка библиотек

pip install python-telegram-bot==20.5
pip install fastapi
pip install python-dotenv
pip install uvicorn
pip freeze > requirements.txt

▶️ Запуск приложения с помощью uvicorn

```bash
uvicorn index:app --reload
```

После запуска приложение будет доступно по адресу:
http://127.0.0.1:8000


📝 Лицензия

