# Flutter for web 環境構築
Flutterのweb版での環境構築です。

## HowTo
1. リポジトリをクローン
    ```
    git clone https://github.com/toshi-click/flutter_test
    ```
1. クローンしたディレクトリで
    ```
    cd flutter_test
    docker-compose build
    ```
1. コンテナを構築、起動
    ```
    docker-compose up -d
    ```
1. 起動したコンテナに入る
    ```
    docker exec -it flutter bash
    ```
1. flutterアプリを作成
    ```
    cd ${APP_CODE_PATH_CONTAINER}
    flutter create .
    ```
1. サーバーを起動
    ```
    flutter run -d web-server --web-port=${WEB_SERVER_PORT} --web-hostname 0.0.0.0
    ```
    下記が表示されたらhttp://localhost:8888にアクセスすればOK
    ```shell
    To hot restart changes while running, press "r" or "R".
    For a more detailed help message, press "h". To quit, press "q".
    ```
1. Flutterをアップグレードする場合
    ```
    flutter upgrade
    ```
1. Webをビルドする場合
    ```
    flutter build web
    ```
