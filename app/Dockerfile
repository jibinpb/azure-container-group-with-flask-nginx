FROM python:slim

RUN mkdir /app
WORKDIR /app

ADD requirements.txt /app
ADD app.py /app
ADD gunicorn_config.py /app

RUN pip3 install -r requirements.txt

EXPOSE 5000
ENTRYPOINT ["gunicorn", "--config", "gunicorn_config.py", "app:app"]