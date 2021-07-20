# Dock4yii PHP-FPM

_Made on the basis of the **laradock/laradock** project_

#### 🚧 Attention: the project is currently under development! 🚧
The project is not yet fully tested. Use at your own risk!

`Now the project is configured for basic, if you want to use with advanced - correct NGINX or APACHE2 configs`

### Docker

https://docs.docker.com/engine/install/

https://docs.docker.com/engine/install/linux-postinstall/

https://docs.docker.com/compose/install/

### Install

1) Place the `dock4yii` folder in your `yii2` project
2) Go to `your project yii2/dock4yii` folder
3) Copy `.env.example` to `.env`

### Configure

1) Examine the `.env` file and arrange the necessary parameters
* If you know what containers you need, you can comment out or delete unnecessary ones in `docker-compose.yml`
* Otherwise, just run the necessary (`Run` section)
2) Depending on the database you are using, configure the file: `docker/DATABASE/docker-entrypoint-initdb.d` (or whatever path you specified in the `.env`)

### Run
1) To start docker and containers use the command that suits you:

**All (Configured)**
```shell
docker-compose up -d
```

or

**Nginx + MySQL (Min)**
```shell
docker-compose up -d workspace php-fpm nginx mysql
```

or

**Nginx + MySQL**
```shell
docker-compose up -d workspace php-fpm nginx mysql memcached redis rabbitmq
```

**Nginx + PgSQL**
```shell
docker-compose up -d workspace php-fpm nginx postgres memcached redis rabbitmq
```

**Apache2 + MySQL**
```shell
docker-compose up -d workspace php-fpm apache2 mysql memcached redis rabbitmq
```

**Apache2 + PgSQL**
```shell
docker-compose up -d workspace php-fpm apache2 postgres memcached redis rabbitmq
```

2) Enter the container (workspace)
```shell
docker-compose exec --user=dock4yii workspace bash
```

3) Initialize as a normal yii2 project

4) You can use the project, it is available at `http://localhost`