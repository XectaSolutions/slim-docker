## Slim Framework Docker Compose File

**Included Applications:**

- PHP with Apache
- Slim Framework Installation
- Composer
- MySQL
- PhpMyAdmin

## How to run

Install Docker or Docker Toolbox from http://www.docker.com

- Clone from Repository

- Change the working directory to the downloaded folder and call docker-compose up

```
docker-compose up
```

or run add the -d option to run it in background.

```
docker-compose up -d
```

This will start the containers and will start the installation of Slim Framework and composer packages. Once the installation is complete you will see the Slim home page in localhost:8080 (or the port you specified in ENV).

Note: If you use docker toolbox, you might need to use the IP address of the docker machine rather than `localhost`

## App Folder

Slim Framework will be installed in a subfolder `app`.

## Database

MySql stores data in local folder `.db_data`. If you delete the folder database contents will be lost. You may ignore the database contents from .gitignore by uncommenting the line in `.git-ignore` file.

```
#To ignore local db changes you may uncomment the following line
#.db_data
```

Default user name is `root` with password `secret`

PhpMyAdmin can be accessed on http://localhost:8081

## Configuration

Edit the .env file and modify as necessary

```
#Select the PHP version

PHP_VERSION=7.2

#Select the MySql Tag. Defaults to latest
#Eg: 5.7

MYSQL_TAG=latest

#Databse and access details

DB_USERNAME=root
DB_PASSWORD=secret

#Change the port for accessing site (Defaults to 8080)
#Eg: 80

SITE_PORT=8080

#Change the port for PhpMyAdmin (To access DB)
#Eg: 8000

MYADMIN_PORT=8081
```

## .gitignore file

A default `.gitignore` file is supplied for ignoring database if rquired. Slim `app` folder will contain the normal `.gitignore` provided by Slim.


```

## Stopping containers

```
docker-compose down
```
