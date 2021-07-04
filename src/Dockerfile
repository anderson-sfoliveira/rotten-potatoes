FROM python:3.8-slim-buster

WORKDIR /app

COPY requirements.txt /app

RUN python -m pip install -r requirements.txt

COPY . /app

EXPOSE 5000

CMD ["gunicorn", "--workers=3", "--bind", "0.0.0.0:5000", "app:app"]

# criando cluster kubernetes:
# k3d cluster create meucluster --servers 1 --agents 2 -p 8080:30000@loadbalancer"
