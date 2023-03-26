FROM python:3.11-slim-bullseye

# Don't create bytecode .pyc files and don't buffer output
ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONBUFFERED=1

WORKDIR /app

COPY requirements.txt .

RUN pip install --upgrade pip && pip install -r requirements.txt

COPY bul ./bul/

WORKDIR /app/bul

EXPOSE 8000

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
