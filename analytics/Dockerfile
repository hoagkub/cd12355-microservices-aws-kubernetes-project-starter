FROM --platform=linux/arm64 python:3.8-slim-buster AS build

COPY . /app

WORKDIR /app

RUN apt update && apt-get install -y build-essential libpq-dev

RUN pip install --upgrade pip setuptools wheel
RUN pip install -r requirements.txt

EXPOSE 5153

CMD ["python", "app.py"] 