# Bookstore

#### Coding Example from "_Django for Professionals_" by William S. Vincent

### Getting-Started

#### Requirements:
- docker
- docker-compose

#### From the root directory execute:
```bash
docker-compose up -d --build
```

#### Then, we need to make migrations:
```bash
docker-compose exec web python /code/app/manage.py makemigrations accounts
docker-compose exec web python /code/app/manage.py makemigrations books
docker-compose exec web python /code/app/manage.py migrate
```

#### Create superuser
```bash
docker-compose exec web python /code/app/manage.py createsuperuser
```