# Укажите базовый образ
FROM python:3.9

# Установите текущую рабочую директорию
WORKDIR /app

RUN groupadd -r ym && useradd -r -g ym ym

# Скопируйте зависимости в рабочую директорию
COPY requirements.txt requirements.txt

# Установите зависимости
RUN pip install -r requirements.txt

# Скопируйте файлы приложения в рабочую директорию
COPY . .

# Укажите порт, на котором запускается приложение
EXPOSE 5000

USER ym

# Задайте команду, которая будет выполняться при запуске контейнера
CMD ["python", "app.py"]
