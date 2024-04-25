FROM python:3.9

WORKDIR /app

COPY . /app

RUN pip install --no-cache-dir -r requirements.txt

EXPOSE 80

ENV REDIS_HOST=redis

CMD ["flask", "run", "--host=0.0.0.0", "--port=80"]
