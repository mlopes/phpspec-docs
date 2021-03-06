インストール
============

PHPSpec は PEAR でインストールしなければなりません。
PEAR (PHP Extension and Application Respository)
とは、PEAR パッケージの管理や配布を簡単に行うための仕組みのことです。
PHP がインストールされていれば、既に PEAR システムも利用できるようになっているでしょう。

PEAR を使用した PHPSpec のインストール
------------------------------------

PHPSpec は、専用の PEAR チャネルで配布されています。
PEAR チャネルシステムはきわめて簡単に使用でき、
PEAR が利用できるところならばどこでも簡単に PHPSpec をインストールできるようになります。
インストールの前に、まず次のコマンドで PHPSpec
のチャネルを登録しましょう。

.. code-block:: bash

    $ sudo pear channel-discover pear.phpspec.net

これで、新しいチャネルについての情報を PEAR から取得します。

パッケージをインストールするには、次のコマンドを実行します。

.. code-block:: bash

    $ sudo pear install phpspec/PHPSpec

.. note::

    PHPSpec の開発版スナップショットは、常に
    `http://github.com/phpspec/phpspec <http://github.com/phpspec/phpspec>`_
    に公開されています。このスナップショットは不安定なものなので、
    テストやフィードバックといった用途以外では用いないでください。
    開発版スナップショットのインストール方法については、以下の
    "手動での PHPSpec のインストール" のセクションを参照ください。

PEAR パッケージをダウンロードすることによる PHPSpec のインストール
------------------------------------------------------------

PEAR チャネルシステムを使わずに PHPSpec をインストールするには、
PEAR パッケージのアーカイブを
`http://pear.phpspec.net/get <http://pear.phpspec.net/get>`_
からダウンロードしたうえで次のコマンドを実行します。

.. code-block:: bash

    $ sudo pear install PHPSpec-<version>.tar.gz

手動での PHPSpec のインストール
-----------------------------

PHPSpec を手動でインストールするには、PEAR パッケージ版ではないアーカイブ
"PHPSpec-<version>.tar.gz" を
`http://pear.phpspec.net/get/nonpear <http://pear.phpspec.net/get/nonpear>`_
からダウンロードします。これを好きな場所に展開し、
その "src" ディレクトリを php.ini の include_path に追加します。
また、"scripts" ディレクトリにあるスクリプト phpspec
(Windows の場合は phpspec.bat)
を、パスの通った場所にコピーします。必要に応じてこのスクリプトを編集し、
PHP バイナリ実行ファイルの場所や PHPSpec
クラスファイルの場所を設定する必要があります。
