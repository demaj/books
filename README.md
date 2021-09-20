# Bookstore

#### Coding Example from "_Django for Professionals_" by William S. Vincent

### Getting-Started

#### Requirements:
- docker
- docker-compose

#### From the root directory execute:
```bash
docker-compose -f docker-compose-local.yml up -d --build
```

#### Then, we need to make migrations:
```bash
docker-compose -f docker-compose-local.yml exec web python /code/app/manage.py makemigrations
docker-compose -f docker-compose-local.yml exec web python /code/app/manage.py migrate
```

#### Create superuser
```bash
docker-compose -f docker-compose-local.yml exec web python /code/app/manage.py createsuperuser
```