# セルフホストする
セルフホストするには、以下のソフトウェアが必要です。また、v1.1.0時点では**MongoDBの認証機能には対応していません。**
> 1.2.0で対応しました。
* Python 3.12系
* MongoDB
* pipenv
* [ffmpeg](https://www.ffmpeg.org/download.html) (オプション、読み上げ機能を利用する場合)

### 1. pipenvで依存関係をインストールする
以下のコマンドを実行して、Seleneの依存関係を導入します。
```bash
$ pipenv install
```
### 2. config.yml.exampleをコピーする
config.yml.exampleをコピーしてconfig.ymlとして保存します。
```bash
$ cp config.yml.example config.yml
```

コピーしたconfig.ymlを開いて、トークンなどを入力します。

必ず編集が必要なのは、database以下と、tokenです。

### 3. 起動する
以下のコマンドで簡単に起動できます。pipenvの環境に入らず`python main.py`を実行するとライブラリ不足でエラーが出ます。
```bash
$ pipenv run start
```