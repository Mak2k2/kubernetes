FROM python:alpine3.16

RUN addgroup -g 2000 userapp \
    && adduser -u 2000 -G userapp -s /bin/sh -D userapp

USER userapp

RUN pip install click==7.1.2 Flask==1.1.2 itsdangerous==1.1.0 Jinja2==2.11.2 MarkupSafe==1.1.1 Werkzeug==1.0.1

WORKDIR /app

COPY ./app.py /app

EXPOSE 8080

ENTRYPOINT python /app/app.py