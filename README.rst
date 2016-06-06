OpenPNE3 標準環境
=================

OpenPNE3 の開発・動作確認に使用する標準の環境を定義するためのプロジェクト

構成
----

* Linux 3.16.7
* Apache 2.4.10
* MySQL 5.5.49
* PHP 5.6.20

2016/5/31 時点における Debian の最新の安定版である jessie (8.4) をベースとしています

必要なミドルウェア等も極力 Debian の main セクションに含まれるパッケージが使われています

OpenPNE のインストール手順に記載されている PHP の拡張モジュールについては「推奨」のものも含めインストールされた状態です

注意
----

* APC 拡張モジュールは PHP 5.6.x に非対応のため、代わりに `APCu <https://secure.php.net/manual/ja/book.apcu.php>`_ 拡張モジュールがインストールされています
* PHP 標準の JSON 拡張モジュールは、DFSG 不適合なライセンスの問題により Debian のリポジトリからは削除されています
  そのため、別の実装である `pecl-json-c <https://pecl.php.net/package/jsonc>`_ が含まれた `php5-json <https://packages.debian.org/jessie/php5-json>`_ パッケージがインストールされています
* この環境には OpenPNE 本体は含まれていません

イメージの生成
--------------

* ``docker build -t openpne/openpne3-env .``

ライセンス
----------

`Apache License Version 2.0 <https://www.apache.org/licenses/LICENSE-2.0>`_

Copyright (c) 2016 Kimura Youichi <yoichi.kimura@tejimaya.com>

生成されたイメージに含まれる各ソフトウェアのライセンスは、イメージ内の ``/usr/share/doc/*/copyright`` を参照してください
