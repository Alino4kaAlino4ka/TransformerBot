# TransformerBot


# TransformerBot - Чат-бот на основе трансформерной модели

TransformerBot - это чат-бот, основанный на fine-tuned версии модели rugpt3small от Сбера, дообученной на датасете SiberianPersonaChat (448k диалогов). Проект включает полный цикл: от обучения модели до развертывания в Telegram.

## 🔹 Особенности

- **Fine-tuned модель**: Дообученная версия rugpt3small с оптимизированными параметрами генерации
- **Интерактивный чат**: Возможность общения в режиме реального времени
- **Telegram-интеграция**: Готовый бот для мессенджера
- **Оценка качества**: Метрики и примеры работы модели

## 🔹 Технологии

- Python 3.8+
- PyTorch
- Transformers (Hugging Face)
- Datasets (Hugging Face)
- Telegram Bot API

## 🔹 Установка и запуск

1. Клонируйте репозиторий:
```bash
git clone https://github.com/ваш-username/TransformerBot.git
cd TransformerBot
```

2. Установите зависимости:
```bash
pip install -r requirements.txt
```

3. Запустите обучение (опционально):
```python
python train.py
```

4. Запустите чат-бота:
```python
python chat.py
```

5. Для Telegram-бота (требуется токен):
```python
python telegram_bot.py
```

## 🔹 Примеры работы

```python
Вопрос: Что такое программирование?
Ответ: Программирование - это процесс создания и редактирования программного обеспечения...

Вопрос: Какой твой любимый фильм?
Ответ: Я обожаю фильм "Титаник". Он такой захватывающий и трогательный...
```

## 🔹 Структура проекта

```
TransformerBot/
├── finetuned_chatbot/        # Сохраненная модель
├── datasets/                 # Данные для обучения
├── train.py                  # Скрипт обучения
├── chat.py                   # Интерактивный чат
├── telegram_bot.py           # Telegram-интеграция
├── evaluate.py               # Оценка модели
└── requirements.txt          # Зависимости
```

## 🔹 Настройки генерации

Параметры можно изменить в коде:
```python
output = model.generate(
    input_ids,
    max_new_tokens=150,
    temperature=0.7,
    top_k=50,
    top_p=0.9,
    repetition_penalty=1.2,
    do_sample=True
)
```

## 🔹 Планы по улучшению

- Увеличение датасета (до 1M+ примеров)
- Добавление штрафа за повторения (repetition_penalty)
- Пост-обработка ответов
- Интеграция более крупных моделей (rugpt3large)

## 🔹 Автор

[Алина Грибанова] - [https://t.me/Alino4kaGribavova]

## 🔹 Лицензия

MIT License
