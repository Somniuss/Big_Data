# Task 1 - Python Introduction

Проект загружает JSON файлы студентов и комнат в MySQL и выполняет аналитику.

---

## Установка

1. Создаем виртуальное окружение
2. Активируем его
3. Устанавливаем зависимости

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
```

### Запуск
```bash
python -m scripts.load_data --students data/students.json --rooms data/rooms.json --format json
```
#### Результат работы

После запуска скрипта приложение:
- Загружает данные из `students.json` и `rooms.json` в базу MySQL.  
- Выполняет аналитические запросы:  
  - Количество студентов в каждой комнате.  
  - 5 комнат с самым маленьким средним возрастом.  
  - 5 комнат с наибольшей разницей в возрасте.  
  - Комнаты с разнополыми студентами.  
- Выводит результаты в формате JSON или XML в консоль.
