1) 概要

このプログラムはtwitterをコマンドラインから扱うためのものです。

2) ライセンス

このプログラムはMITライセンスの下で配布します。なお、 OAuth.php と twitteroauth.php は abraham さんによるプログラムです(http://github.com/abraham/twitteroauth)。

3) 動作環境

次の環境で動作確認を行っています。

- MacOSX
- PHP 5.2.x (--with-curl でコンパイルしたもの)

4) 設定

まず、設定ファイルのサンプルである twitter.ini.sample を twitter.ini という名前にコピーします。

$ cp twitter.ini.sample twitter.ini

このプログラムはtwitterのOAuth機能を使用します。そのため、あらかじめ、 dev.twitter.com (http://dev.twitter.com/apps/) にてアプリケーション登録を済ませておく必要があります。アプリケーション登録をすると、"Consumer Key"、 "Consumer Secret"、 "Access Token"、"Access Token Secret" を取得できるので、それらを twitter.ini に設定してください。

5) 使用方法

$ twitter_cui	-mode=post "tweetしたい文字列"
$ twitter_cui	-mode=post -to=123456789 "@foobarポストid=123456789への返信"
$ twitter_cui -mode=list リスト名
$ twitter_cui -mode=mention # 自分あてのmentionを見る

5) 未実装機能

以下は未実装の機能です(導入時期は未定)。

- 素のタイムラインの取得
- ダイレクトメールの送受信
- favoriteの送受信
- 検索
- などなど
