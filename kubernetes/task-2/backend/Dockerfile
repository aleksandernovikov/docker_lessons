# ОБЯЗАТЕЛЬНО. Родительский образ
FROM python:3.6

# НЕ ОБЯЗАТЕЛЬНО. Настройка образа для работы приложения. Копирование необходимых файлов. Самого приложения.
COPY . /app
COPY entrypoint.sh /usr/local/bin/
RUN chmod +x /usr/local/bin/entrypoint.sh
RUN pip install -r /app/requirements.txt

# Не обязательно. Тут мы прописываем какая папка будет точкой входа в docker контейнер.
WORKDIR /app

# Тут мы описываем что и как запустить на старте контейнера. entrypoint.sh можно считать как конструктор.
ENTRYPOINT ["entrypoint.sh"]
CMD ["python", "app.py"]
