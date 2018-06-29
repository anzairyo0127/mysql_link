# 課題点
1.`busy box`等がないため、データの永続化はできておりません。

2.`ignored in --skip-name-resolve mode`という`Warning`メッセージの解決が済んでおりません。

# 事前準備

1.`example.env`を`.env`にrename

2.`.env`を編集する


# クイックスタート
Docker Composeでimageの作成、containerの起動まで行いますので

カレントディレクトリをdocker-compose.ymlのある場所まで移動してから

`docker-compose up`にて立ち上げてください。

立ち上がるcontainerは2つです。

`docker_app_1`　こちらがmysqlのクライアント側になります。

`docker_db_1`　 こちらがmysqlのサーバー側になります。

`docker exec -it docker_app_1 /bin/bash`コマンドを実行してください。

`docker_app_1`container内に侵入したら

`mysql -h docker_db_1 -p`とコマンドを実行してください。

passwordを問われますので`MYROOT_PASS`と打てば通ります。

`mysql >`と表示されればOK
