# Cloudlog-dockers

## DO NOT USE IN PRODUCTION

Cloudlog-dockers provides a docker development environment for [Cloudlog](https://github.com/magicbug/Cloudlog).

## Requirements
* docker
* docker-compose
* Nothing running on ports 80 and 8080

Please note: only tested in Linux

## Setup

(Assuming a new Cloudlog clone)
Clone the project alongside Cloudlog, ie:

```
$ ls
Cloudlog  Cloudlog-dockers
```

Then startup the dockers
```
cd Cloudlog-dockers
docker-compose up -d
```

Point your browser to `http://localhost` and follow the instructions for a new installation.
At the end of the installation ignore the errors related with unlinking files.

Write enable the uploads directory
```
chmod uga+w ../Cloudlog/uploads
```

Your dev environment is now ready.

## Usage

#### Running the environment
```
cd Cloudlog-dockers
docker-compose up -d
```

#### Stopping the environment
```
cd Cloudlog-dockers
docker-compose up -d
```


#### Opening a shell on the web server
`docker exec -it cloudlog-dockers_web_1 /bin/bash`

#### Opening mysql on the db
`docker exec -it cloudlog-dockers_db_1 mysql -u user -p` (password is password)

#### Running phpMyAdmin
point your browser to `http://localhost:8080`