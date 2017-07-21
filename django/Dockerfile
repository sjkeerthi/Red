FROM ubuntu:16.04

RUN apt-get update && apt-get install -y language-pack-en language-pack-en-base git libmysqlclient-dev python3 python3-pip

ENV PYTHONUNBUFFERED 1

RUN mkdir -p /trunk/django

WORKDIR /trunk/django

ADD requirements /trunk/django/

RUN pip3 install -r /trunk/django/requirements

VOLUME /trunk/django 

CMD python3 manage.py runserver 0.0.0.0:8000

EXPOSE 8000
