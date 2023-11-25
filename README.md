# sandbox-for-isucon
isuconのサンドボックス

## 環境構築
```bash
$ docker compose -f infra/docker-compose.yml build
```
### appの環境構築(gemの導入)
```bash
$ bin/exec-bash app
$ bundle install
```

## mysql2の実行
```ruby
client = Database::Client.connect_db
client.xquery('show databases;')
```

## tips
```bash
$ bin/exec-bash app
```

```bash
$ bin/exec-bash database
```
