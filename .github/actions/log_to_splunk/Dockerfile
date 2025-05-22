FROM python:3.9-slim

# Fix the ENV format warning
ENV PYTHONUNBUFFERED=1

RUN pip install --no-cache-dir requests

COPY . /app
WORKDIR /app
RUN chmod +x /app/main.py

ENTRYPOINT ["python", "/app/main.py"]
