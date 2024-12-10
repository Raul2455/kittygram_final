FROM python:3.9

WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

ENV DJANGO_SETTINGS_MODULE=kittygram_backend.settings

CMD ["gunicorn", "--bind", "0.0.0.0:8080", "kittygram_backend.wsgi:application"]
