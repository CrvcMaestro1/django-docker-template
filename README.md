# Django - PostgreSQL - Gunicorn - Nginx

Template to dockerizer projects with multiple stages [DEV, PROD]

# DEV Commands

- ## Build and Up

  ``docker-compose -f docker-compose.dev.yml up -d --build``

- ## Migrate

  ``docker-compose -f docker-compose.dev.yml exec web python manage.py migrate --noinput``

- ## Collectstatic

  ``docker-compose -f docker-compose.dev.yml exec web python manage.py collectstatic --no-input --clear``

- ## Down with volumes

  ``docker-compose -f docker-compose.dev.yml down -v``

- ## Down without volumes

  ``docker-compose -f docker-compose.dev.yml down``

# PROD Commands

- ## Build and Up

  ``docker-compose -f docker-compose.prod.yml up -d --build``

- ## Migrate

  ``docker-compose -f docker-compose.prod.yml exec web python manage.py migrate --noinput``

- ## Collectstatic

  ``docker-compose -f docker-compose.prod.yml exec web python manage.py collectstatic --no-input --clear``

- ## Down with volumes

  ``docker-compose -f docker-compose.prod.yml down -v``

- ## Down without volumes

  ``docker-compose -f docker-compose.prod.yml down``

# Appreciation to [Dockerizing Django with Postgres, Gunicorn, and Nginx](https://testdriven.io/blog/dockerizing-django-with-postgres-gunicorn-and-nginx/) tutorial.
