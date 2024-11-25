# Client Records Telegram Bot

Бот для записи клиентов и предоставления информации о продуктах и услугах.

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

```bash
client-records-telegram-bot/
│
├── api/
│   └── index.py             # Основной файл с кодом бота
├── venv/                    # Виртуальное окружение (не добавляйте в Git)
├── .gitignore               # Исключение виртуального окружения из репозитория
├── requirements.txt         # Зависимости проекта
├── vercel.json              # Конфигурация Vercel для маршрутизации
├── README.md                # Документация для проекта (опционально)
└── .env                     # Переменные окружения (не для публичного репозитория)
```

## 🚀 Установка и настройка

### 1. Клонируйте репозиторий

```bash
git clone https://github.com/your-username/client-records-telegram-bot.git
cd client-records-telegram-bot
```
### 2. Установка Homebrew для Linux/MacOS

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

brew --version
```

Apple Silicon (M1/M2):
```bash
echo 'eval "$(/usr/local/bin/brew shellenv)"' >> ~/.zshrc
eval "$(/usr/local/bin/brew shellenv)"
```

Intel:
```bash
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zshrc
eval "$(/opt/homebrew/bin/brew shellenv)"
```

Установка python
```bash
brew install python
python --version
```

Установка Node.js
```bash
brew install node
node --version
npm --version
```

### 3. Установите виртуальное окружение и зависимости

```bash
python3 -m venv venv             # Создаем виртуальное окружение в папке `venv`
source venv/bin/activate         # Активируем виртуальное окружение (Linux/MacOS).
venv\Scripts\activate            # Активируем виртуальное окружение на Windows.
```

```bash
pip --version                # Проверяем текущую установленную версию `pip` (пакетного менеджера Python)
pip install --upgrade pip    # Обновляем `pip` до последней версии
```

```bash
pip install -r requirements.txt  # Устанавливаем все зависимости, указанные в файле `requirements.txt`
```

📦 Установка библиотек

```bash

# Устанавливаем библиотеку для работы с Telegram Bot API (версия 20.5)
pip install python-telegram-bot==20.5

# Устанавливаем FastAPI — фреймворк для создания веб-приложений и API
pip install fastapi

# Устанавливаем библиотеку для работы с переменными окружения из файла `.env`
pip install python-dotenv

# Устанавливаем Uvicorn — ASGI-сервер для запуска FastAPI-приложений
pip install uvicorn

# Сохраняем текущие установленные зависимости в файл `requirements.txt`
# Это позволяет другим разработчикам установить те же версии библиотек
pip freeze > requirements.txt


pip install httpx

pip install requests
```

▶️ Настройте вебхук для Telegram

Установите сервер Vercel CLI

```bash
npm install -g vercel
vercel --version
```
Авторизуйтесь в Vercel

```bash
vercel login
```

Создайте конфигурацию vercel.json

```json
{
  "routes": [
    { "src": "/.*", "dest": "api/index.py" }
  ]
}
```

Разверните проект сделайте деплоя в Vercel

```bash
vercel
```

▶️ Запуск приложения с помощью uvicorn

```bash
uvicorn index:app --reload
```

После запуска приложение будет доступно по адресу:
http://127.0.0.1:8000

