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
## Access URL
http://localhost:8000/

