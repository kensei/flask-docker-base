FROM python:3.7-alpine

RUN apk add --update --no-cache bash git vim tzdata \
 && cp /usr/share/zoneinfo/Asia/Tokyo /etc/localtime \
 && echo "Asia/Tokyo" > /etc/timezone \
 && apk del tzdata
ENV LANG ja_JP.UTF-8
ENV LANGUAGE ja_JP:ja
ENV LC_ALL ja_JP.UTF-8
ENV TZ JST-9

RUN pip install --upgrade pip setuptools

WORKDIR = /app
COPY requirements.txt /app/requirements.txt
RUN pip install -r /app/requirements.txt

CMD ["python", "/app/test.py"]
