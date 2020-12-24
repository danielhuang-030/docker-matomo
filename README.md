# docker-matomo

### Introduction
Docker for [matomo](https://matomo.org/)

### Including
 - [matomo](https://hub.docker.com/_/matomo)
 - [MariaDB](https://hub.docker.com/_/mariadb)
 - [phpMyAdmin](https://hub.docker.com/r/phpmyadmin/phpmyadmin)

### Usage

```shell
# start docker
docker-compose up -d

# stop docker
docker-compose down

# docker logs
docker-compose logs -f
```

### Config
```shell
./dockerize/config/matomo/config.ini.php
```

### Port
| service  | port-inside | port-outside  | description |
|---|---|---|---|
| matomo  | - | 60080 | [matomo](http://localhost:60080) | 
| matomo-db | 3306, 33060 | 60006 | MariaDB |
| matomo-pma | 80 | 60010 | [phpMyAdmin](http://localhost:12010) |

### Password
| Service  | Username | Password  | 
|---|---|---|
| matomo-db | root | root |
