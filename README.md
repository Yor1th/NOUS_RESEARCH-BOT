![NOUS Banner](https://github.com/NotHennadii/NOUS_RESEARCH-BOT/blob/main/652724572457.PNG?raw=true)


## UPDATE ВЕРСИЯ 3.1
Поддерживаются 4 модели с разной вероятностью.
Вопросы теперь создаются только через API, язык — по выбору: русский, английский, или оба.
Старые RANDOM_QUESTIONS удалены.
Указана величена токена, чтобы сократить затраты на дистанции
Переработан сам скрипт , значительно уменьшено потребление токенов


## 📦 Установка и запуск WINDOWS

1. **Дублировать или скачать файлы в папку**

2. **Создай файл `start.bat`** (если ещё нет,а он ЕСТЬ!):

```bat
@echo off
python -m venv venv
call venv\Scripts\activate
pip install -r requirements.txt
python NOUS.py
```

3. **Подготовь файлы в корне проекта:**

* `API_keys.txt` — список API ключей (по одному в строке):

  ```
  sk-abcdef...
  sk-xyz123...
  ```

* `proxy.txt` — список прокси (если используешь), в любом из форматов:

  ```
  http://user:pass@ip:port
  user:pass:ip:port
  ```

* `promt.txt` — системный промпт для AI (можно оставить пустым):

  ```
  Ты — мудрый помощник, дающий краткие и умные ответы.
  ```

---

## 🚀 Запуск

Запусти `start.bat` — при первом запуске он создаст venv, установит зависимости и запустит бота.

---

## 🛠️ Параметры запуска

В консоли укажи:

| Вопрос                       | Пример ответа |
| ---------------------------- | ------------- |
| Кол-во запросов на поток     | `5`           |
| Кол-во потоков               | `3`           |
| Использовать прокси (y/n)    | `y` или `n`   |

---

## 📑 Что делает бот

* Запускает многопоточную отправку запросов к DeepHermes
* Использует ключи из `API_keys.txt` циклично
* Генерирует **уникальные вопросы через AI**
* Поддерживает **рандомные задержки**
* Выводит лог с таймингами и прогрессом
* Сохраняет ответы в `log.txt`

---

## ✅ Пример логов

![token Banner](https://github.com/NotHennadii/NOUS_RESEARCH-BOT/blob/main/624565247245.PNG?raw=true)

---

## 🔥 Зависимости

Указаны в `requirements.txt`:

```
requests
web3
rich
aiohttp
```

---

# 🚀 NOUS Research Bot - Установка на macOS

## 📋 Быстрая установка

### 1. Предварительные требования
- macOS 10.14 или новее
- Python 3.7+ (обычно уже установлен)

### 2. Проверьте Python
Откройте Terminal и выполните:
```bash
python3 --version
```

Если Python не установлен, установите через Homebrew:
```bash
# Установка Homebrew (если нет)
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Установка Python
brew install python
```

### 3. Подготовка файлов
1. Скопируйте все файлы в одну папку:
   - `NOUS.py`
   - `requirements.txt`
   - `start.sh`

2. Откройте Terminal и перейдите в папку с файлами:
   ```bash
   cd /путь/к/вашей/папке
   ```

3. Сделайте скрипт исполняемым:
   ```bash
   chmod +x start.sh
   ```

### 4. Настройка API ключей
Создайте файл `API_keys.txt` и добавьте ваши ключи:
```
your_api_key_1
your_api_key_2
your_api_key_3
```

### 5. Запуск
Просто выполните:
```bash
./start.sh
```

## 📁 Структура файлов
```
project_folder/
├── NOUS.py              # Основной скрипт
├── requirements.txt     # Зависимости Python
├── start.sh            # Скрипт запуска для macOS
├── API_keys.txt        # Ваши API ключи
├── promt.txt           # Системные промпты (опционально)
└── proxy.txt           # Прокси (опционально)
```

## 🛠️ Альтернативный запуск
Если что-то не работает, можете запустить вручную:

```bash
# Создание виртуального окружения
python3 -m venv venv

# Активация
source venv/bin/activate

# Установка зависимостей
pip install -r requirements.txt

# Запуск
python3 NOUS.py
```

## 🚨 Возможные проблемы

### Ошибка "Permission denied"
```bash
chmod +x start.sh
```

### Python не найден
Установите Python через официальный сайт или Homebrew

### Ошибки с SSL
```bash
pip install --upgrade certifi
```

## 💡 Советы
- Держите файлы в одной папке
- Регулярно обновляйте API ключи
- Используйте `Ctrl+C` для остановки скрипта
- Логи сохраняются в `ai_stress_log.txt`

## 🎯 Готово!
Теперь вы можете запускать скрипт простой командой `./start.sh`


## 🧬 Лицензия

> Эта штука сделана ради науки, экспериментов и фана.
> Используй на свой страх и страх.
