# Knowledge-composed

# これは何？

ナレッジベースシステム`knowledge`とpostgresqlを、docker-composeで構成するための`docker-compose.yml`です。

# 使い方

`docker-compose up`等で起動してください。
起動時にデータボリュームコンテナ(`dataコンテナ`)内にknowledgeの設定が残っていない場合、
DBへの接続設定を行わないと、knowledgeとDBの接続が行われません。
管理者でログインして、DB接続設定を行って下さい。（つまり初回の接続は手動で行う必要があるということです）

## DB接続設定例 (このリポジトリのdokcer-compose.ymlを使った場合のデフォルト設定)

* URL				: jdbc:postgresql://psql:5432/knowledgebase
* user				: knowledge
* password			: password
* schema			: knowledgebase
* max connection	: 0
* auto commit		: false
