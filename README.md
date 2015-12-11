# docker-centos7-php

PHP-FPM image running on CentOS 7 preconfigured to work along with NGINX and MySQL images.

Mount the root folder:

```yaml
  volumes:
    - ./src/public:/var/www/public
```


Link to an optional MySQL/MariaDB server:

```yaml
  links:
    - mysql
```


You can set the environment vars:

```yaml
  env_file:
    - './db.env'
  environment:
    MYSQL_HOST: "mysql"
```


db.env file example:

```
# db.env
MYSQL_ROOT_PASSWORD=MyRoot
MYSQL_DATABASE=MyDB
MYSQL_USER=MyUser
MYSQL_PASSWORD=MyPassword
```