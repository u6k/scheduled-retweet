# scheduled-retweet

公式リツイートを予約実行します。

## 概要

ツイートの予約実行はHootSuiteなどでできますし、分散しても良いなら公式リツイートの予約はBufferでできますが、時刻を指定しての公式リツイートができるサービスが見つかりませんでした。なので、(あくまで自分用ですが)公式リツイートを予約実行するアプリケーションを作成します。

## 使い方

### Twitterと連携する

* OAuthで連携して、トークンを取得する。

> *TODO:* トークンの保存先は、クライアント？サーバー？

### 公式リツイートを予約する

* URL: /retweet/schedule
* メソッド: POST
* パラメータ
    * url: リツイートするツイートのURL。
    * datetime: リツイートする時刻のUnix時刻。
* レスポンス・コード
    * 201 Created: 成功。
    * 400 Bad Request: パラメータが不正。
    * 401 Unauthorized: Twitterにログインしていない。
* レスポンス・ボディ
    * なし。

> *TODO:* パラメータでトークンも渡すべきか？

## 課題管理

https://myredmine-u6kapps.rhcloud.com/projects/scheduled-retweet
