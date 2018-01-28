# README
DokerでRails環境を構築してみたサンプルアプリです。

# 使い方
下記コマンドを実行して、`localhost:3000`にアクセスするとRailsのスタートページが表示されます。
```
$ git clone https://github.com/Madogiwa0124/docker_sample_app.git
$ docker-compose up
```

# tips
## スタートページアクセス時にDB関係のエラーが出る
DBが未作成、マイグレーションが未実行の可能性がありますで、`wev_server`のコンテナ上で下記コマンドを実行してみてください。
```
$ rails db:create
$ rails db:migrate
``` 

## コンテナ起動時にdockersampleapp_web_server_1 exited with code 1が発生する
`tmp/pids/server.pid`を削除して再度、`docker-compose up`を実行してみてください。

