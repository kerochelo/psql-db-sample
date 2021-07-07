# コンテナ作成&起動
```
$ docker-compose up -d
```

# init database(最初だけ)
```
$ docker exec postgres psql -U postgres -c "create database dvdrental"
$ docker exec postgres pg_restore -U postgres -d dvdrental /tmp/data/dvdrental.tar
```

# postgresコンテナ接続
```
$ docker exec -it postgres psql -U postgres -d dvdrental
```

# コンテナ停止
```
$ docker-compose stop
```

# バルス
```
$ docker-compose down --rmi all --volumes --remove-orphans
```
