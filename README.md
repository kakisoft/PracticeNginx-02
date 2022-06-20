# PracticeNginx-02
PracticeNginx-02  

PHP を追加。


## containers running / terminating
```
docker-compose up -d
docker-compose down
```


## containers login
```
docker-compose exec --user root nginx bash
docker-compose exec --user root php bash
```


## delete containers after terminating
```
docker-compose down --rmi all
docker-compose down --rmi all --volumes
```

________________________________________________________________________________________
## vi install
```
apt-get update
apt-get install -y vim
```

## ping install
```
apt-get update
apt-get install -y iputils-ping
```
____________________________________________________________
## Access
http://localhost:8000/


## PHP Accesscheck
```
ping php
```


## log
```
/var/log/nginx/access.log
/var/log/nginx/error.log
```

________________________________________________________________________________________
________________________________________________________________________________________
________________________________________________________________________________________
________________________________________________________________________________________
________________________________________________________________________________________



