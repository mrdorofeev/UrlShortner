FROM python:alpine

RUN mkdir app

WORKDIR app

COPY . /app

RUN pip install -r requirements.txt

FROM alpine:3.19

RUN apk add --no-cache sqlite

WORKDIR /database

CMD gunicorn urlshortner.wsgi:application -b 0.0.0.0:8000
