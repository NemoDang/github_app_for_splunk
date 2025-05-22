FROM registry.access.redhat.com/ubi8/python-39
USER root

RUN pip install --no-cache-dir requests

COPY . /app
WORKDIR /app

ENTRYPOINT ["python", "/app/main.py"]
