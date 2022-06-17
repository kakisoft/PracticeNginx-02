# PracticeNginx-02
PracticeNginx-02  

PHP


## containers running / terminating
```
docker-compose up -d
docker-compose down
```


## containers login
```
docker-compose exec --user root nginx bash
```


## delete containers after terminating
```
docker-compose down --rmi all
docker-compose down --rmi all --volumes
```

____________________________________________________________
## Access
http://localhost:8000/



/etc/nginx/nginx.conf

/var/log/nginx/access.log

















接続がリセットされました

ページの読み込み中にサーバーへの接続がリセットされました。

    このサイトが一時的に利用できなくなっていたり、サーバーの負荷が高すぎて接続できなくなっている可能性があります。しばらくしてから再度試してください。
    他のサイトも表示できない場合、コンピューターのネットワーク接続を確認してください。
    ファイアウォールやプロキシーでネットワークが保護されている場合、Firefox によるウェブアクセスが許可されているか確認してください。


-----------------------------

正常に接続できませんでした

localhost:8000 のサーバーへの接続を確立できませんでした。

    このサイトが一時的に利用できなくなっていたり、サーバーの負荷が高すぎて接続できなくなっている可能性があります。しばらくしてから再度試してください。
    他のサイトも表示できない場合、コンピューターのネットワーク接続を確認してください。
    ファイアウォールやプロキシーでネットワークが保護されている場合、Firefox によるウェブアクセスが許可されているか確認してください。


=========================================================================

https://zukucode.com/2019/06/docker-compose-nginx-php.html

fastcgi_pass
が重要みたい


https://zenn.dev/harachan/articles/cfa569b8c2175e
PHPコンテナが入ってる事が前提？

ping php



https://kitigai.hatenablog.com/entry/2019/05/01/024341
※FastCGIサーバではデフォルトポートの9000番を使用するためportsの指定は行いません。








PracticeNginx-01
PracticeNginx-02

