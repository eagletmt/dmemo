# Dmemo ![travis-ci](https://travis-ci.org/hogelog/dmemo.svg)
Database description management tool.


## Setup
```
$ bundle install
$ ./bin/rake bower:install
$ ./bin/rake db:create
$ ./bin/rake ridgepole:apply
$ ./bin/rails s
```

### Docker

Docker images published on Docker Hub.
https://hub.docker.com/r/hogelog/dmemo/

```
$ cp .env.sample .env.docker
$ vi .env.docker
...
$ docker run --rm --env-file .env.docker -t hogelog/dmemo ./bin/docker_db_apply.sh
$ docker-compose up
```

## Configure
### Create Admin User
- Login dmemo by google account
- Activate user as admin
```
$ ./bin/rake admin:activate EMAIL=konbu.komuro@gmail.com
 or
$ docker run --env-file .env.docker hogelog/dmemo ./bin/docker_admin_activate.sh konbu.komuro@gmail.com
```
