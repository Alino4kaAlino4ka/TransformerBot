# TransformerBot 

 
# TransformerBot - Чат-бот на основе трансформерной модели
 
TransformerBot - это чат-бот, основанный на fine-tuned версии модели rugpt3small от Сбера, дообученной на датасете SiberianPersonaChat (448k диалогов). Проект включает полный цикл: от обучения модели до развертывания в Telegram. 

https://colab.research.google.com/drive/1LHlmVI4_fN0OtxhN2lqGMMCNUICbAS3K#scrollTo=XXbVXXV6u88p

 
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



## 🔹 Примеры работы

```python
Вопрос: Что такое программирование?
Ответ: Программирование - это процесс создания и редактирования программного обеспечения...

Вопрос: Какой твой любимый фильм?
Ответ: Я обожаю фильм "Титаник". Он такой захватывающий и трогательный...
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
