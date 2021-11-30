# syntax=docker/dockerfile:1

# Reference: https://hub.docker.com/_/python
FROM python:3.8-slim-buster

WORKDIR /app

COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt

COPY . .

CMD [ "python3", "app.py"]

EXPOSE 8080