
FROM alpine:3.4

RUN apk update && apk add py-pip libpq python-dev curl

RUN pip install flask==0.10.1 python-consul

ADD / /app

WORKDIR /app

HEALTHCHECK CMD curl --fail http://localhost:5000/health || exit 1

EXPOSE 5000

CMD ["python", "app.py"]
