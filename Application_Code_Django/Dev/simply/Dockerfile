FROM python:3.11-bookworm

ENV PYTHONUNBUFFERED=1

WORKDIR /django

COPY requirements.txt .

RUN pip3 install --no-cache-dir -r requirements.txt

COPY . .

EXPOSE 8000

CMD ["gunicorn", "simply.wsgi:application", "--bind", "0.0.0.0:8000"]
