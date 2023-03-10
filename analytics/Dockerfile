FROM python:3.8-slim-buster

COPY . /app

WORKDIR /app

RUN apt update && apt-get install -y build-essential libpq-dev

RUN pip install --upgrade pip setuptools wheel
RUN pip install -r requirements.txt

# ARG POSTGRES_PASSWORD=hcupgoan

# ENV DB_USERNAME=hoagkub_u
# ENV DB_PASSWORD=${POSTGRES_PASSWORD}
# ENV DB_HOST=127.0.0.1
# ENV DB_PORT=5432
# ENV DB_NAME=hoagkub_psql

EXPOSE 5153

CMD ["python", "app.py"]