# What is Celery?
- Rather than having to block a response that contains a long-running process, celery can return an HTTP response back immediately and run the process as a background task

## Celery Setup
![Celery Setup](https://github.com/Raihan-009/flask-celery/blob/main/celery-setup.png)

## Run Flask App
```bash
FLASK_APP=app.py flask run
```

## Run Celery Worker
```bash
celery -A app.celery worker --loglevel=info
```

## Sending a task to celery via shell
```bash
FLASK_APP=app.py flask shell
```

## Monitoring Celery with Flower
```bash
celery -A app.celery flower --port=5555
```