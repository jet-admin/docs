# Superuser acess

Normally you don't need to have access to **Jet Admin** database with project and users configuration, but if somehow need to modify it you can get superuser access to built-it admin panel over **Jet Admin** instance.

1. In order to create super user exec the following command on **backend** service:

```
# for Docker Compose
docker-compose exec backend sh
python manage.pyc createsuperuser

# for Kubernetes Dashboard open command line for backend service
python manage.pyc createsuperuser
```

This command will ask you to enter **Username** (should be the same as Email), **Email** and **Password**. If user with such **Email** is already created please use another **Email** for superuser.

2\. Go to **https://\[YOUR\_BACKEND\_URL]/admin/** to access admin panel

