# SQLの砂場環境の構築
## 環境
MySQL 8.0.30
Docker(Debian)
## setup方法
```bash
# dockerのDBコンテナの立ち上げ。
$ docker compose up -d

# コンテナに入る。
$ docker exec -it database bash

# コンテナ内でMySQLクライアントを使う。
$ mysql -u root -proot
```

## dumpの取り方
```
# user_nameはroot、passwordもrootとする。

# 全てのdumpを取りたい場合
$ mysqldump -u root -proot [データベース名] > dump.sql

# dumpを元に復元する場合
$ mysql -u root -proot [データベース名] < dump.sql
```

### 実行例
```bash
$ mysqldump -u root -proot isucondition > dump.sql
```
