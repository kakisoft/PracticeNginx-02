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
## Util Package install
※OS(Debian)のバージョンに注意

### vi install
```
apt update
apt install -y vim
```

### ping install
```
apt update
apt install -y iputils-ping
```


________________________________________________________________________________________
## Access URL
http://localhost:8000/


________________________________________________________________________________________
### Nginx：コンフィグファイルをチェック
nginx -t
```
（出力例）
nginx: the configuration file /etc/nginx/nginx.conf syntax is ok
nginx: configuration file /etc/nginx/nginx.conf test is successful
```

### Nginx：バージョン確認
nginx -V
```
（出力例）
nginx version: nginx/1.15.6
built by gcc 6.3.0 20170516 (Debian 6.3.0-18+deb9u1)
built with OpenSSL 1.1.0f  25 May 2017
TLS SNI support enabled
configure arguments: （以下略）
```
## Nginx：プロセスの状態を確認
nginx -t
nginx -T  （長い）
```
（出力例）
nginx: the configuration file /etc/nginx/nginx.conf syntax is ok
nginx: configuration file /etc/nginx/nginx.conf test is successful
# configuration file /etc/nginx/nginx.conf:

※長ったらしくて見づらい
```

### 再起動
nginx


### 停止（実行したらコンテナが落ちる？）
nginx -s stop




## nginx log
```
/var/log/nginx/access.log
/var/log/nginx/error.log
```


____________________________________________________________
## PHP Accesscheck
※ping コマンドをインストールしておく
```
ping php
```



________________________________________________________________________________________
________________________________________________________________________________________
________________________________________________________________________________________
________________________________________________________________________________________
________________________________________________________________________________________
## note
Docker コンテナ内で nginx コマンドを叩いて再起動したりするのは、止めといた方が良さそう。  
コンテナそのものを再起動で。  

Nginx のコンテナは最新のバージョン or latest を指定。  
OSのバージョンのせいか、aptが上手く動かない（パッケージのいくつかが Not Found）
# image: nginx:1.15.6    # パッケージが古いせいか、aptが上手く動かない（パッケージのいくつかが Not Found）
