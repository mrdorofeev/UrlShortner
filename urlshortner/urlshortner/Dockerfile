FROM python:alpine

RUN mkdir app
WORKDIR app

RUN pip install -r requirements.txt

CMD gunicorn urlshortner.wsgi:application -b 0.0.0.0:8000



