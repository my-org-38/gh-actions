FROM python:3.12.13-alpine

WORKDIR /app

COPY requirements.txt .

RUN pip install --no-cache-dir -r  requirements.txt

COPY . .

RUN addgroup -g 1000 appuser && adduser -D -u 1000 -G appuser appuser

USER appuser

CMD [ "python", "/app/main.py" ]
