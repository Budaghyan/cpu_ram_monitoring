FROM python:3.8-slim

RUN pip install flask pika

WORKDIR /app
COPY app.py .
COPY templates ./templates

CMD ["python", "app.py"]
