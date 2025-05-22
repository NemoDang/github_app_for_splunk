FROM registry.access.redhat.com/ubi8/python-39

# Fix the ENV format warning
ENV PYTHONUNBUFFERED=1

RUN pip install --no-cache-dir requests

COPY . /app
WORKDIR /app
RUN chmod +x main.py

ENTRYPOINT ["python", "/app/main.py"]
