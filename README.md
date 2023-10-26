# Proyecto bomberos voluntarios

## Setup

```bash
# Debemos de crear el archivo .env

# Aquí se debe colocar la secret key que le servirá a Django.
SECRET_KEY=CHANGE_ME
# Aquí debemos de indicar que el servidor a lanzar no estará en modo de desarrollo.
DEBUG=FALSE
```

```bash
# default setup
docker compose exec web python manage.py collectstatic
docker compose exec web python manage.py makemigrations
docker compose exec web python manage.py migrate
docker compose exec web python manage.py create_default_groups
```

## TODO
- Finalizar el apartado de `Acerca de`
- Arreglar permisos
  - Crear los roles y permisos mediante comando de managment
- [X] [Empaquetar la aplicación](https://testdriven.io/blog/dockerizing-django-with-postgres-gunicorn-and-nginx/)
- [ ] Crear worker para realizar guardado de la base de datos

