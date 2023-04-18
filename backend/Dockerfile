FROM tiangolo/uvicorn-gunicorn-fastapi:python3.8

RUN mkdir app
WORKDIR /app

COPY ./requirements.txt .

RUN pip install --no-cache-dir -r /app/requirements.txt

COPY src/ .