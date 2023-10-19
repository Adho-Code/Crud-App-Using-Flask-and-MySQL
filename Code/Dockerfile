## base image
FROM ubuntu:latest

## set environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

WORKDIR /app

RUN apt-get update && \
    # apt-get install -y software-properties-common && \
    apt-get install -y python3 python3-pip && \
    apt-get remove python3-blinker -y

RUN  pip install --upgrade pip
ADD ./requirements.txt /app
RUN pip install -r requirements.txt

COPY . /app


EXPOSE 8000
ENTRYPOINT ["flask", "run","--host=0.0.0.0"]