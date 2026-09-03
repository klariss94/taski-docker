# Базовый образ с Python 3.12
FROM python:3.12

# Установка рабочей директории
WORKDIR /app

RUN pip install gunicorn==25.3.0

# Установка зависимостей
COPY requirements.txt .
RUN pip install -r requirements.txt --no-cache-dir

# Копирование исходного кода
COPY . .

# Запуск сервера
CMD ["gunicorn", "--bind", "0.0.0.0:8000", "backend.wsgi"]
