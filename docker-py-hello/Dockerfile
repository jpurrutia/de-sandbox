FROM python:3.11.4-slim-bullseye

#WORKDIR . app.py /app/
LABEL maintainer="JP Urrutia"
LABEL description="Python Flask API"

RUN mkdir -p /docker-py-hello/src

WORKDIR /docker-py-hello/src

COPY requirements.txt /docker-py-hello/src
COPY . /docker-py-hello/src

RUN pip install --no-cache-dir --upgrade pip \
    && pip install --no-cache-dir -r requirements.txt

ENV APP_ENV development

EXPOSE 8080

CMD ["python", "app.py"]
