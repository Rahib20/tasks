
FROM python:3.11-slim


WORKDIR /app

COPY . .

RUN apt-get update && apt-get install -y \
    gcc \
    default-libmysqlclient-dev \
    pkg-config \
    && rm -rf /var/lib/apt/lists/*

RUN pip install --upgrade pip
RUN pip install -r requirements.txt


ENV ENV=DEV
ENV PYTHONPATH=/app

EXPOSE 5000

CMD ["python", "app.py"]
