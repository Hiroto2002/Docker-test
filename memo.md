# docker

## docker file
コンテナをイメージ化する際に使われる。
これをbuildすることでイメージになる

最終的に他のパソコンやサーバに移動させることもできる

編集した際、docker compose buildで再ビルドが必要
### RUN
build時に実行させたいコマンド

### docker-php-ext-install
PHPの拡張モジュールを入れる

## docker compose
構築にかかわるコマンド分の内容を一つのテキストファイルに書き込んで、一気に実行したり、停止・破棄できるもの
.yaml 形式のファイル内に定義し、up で一括実行、downで一括削除

docker-compose.ymlをカレントディレクトリにし docker-compose up -dで実行

### docker compose up -d
コンテナの起動

### docker compose exec (サービス名)（コンテナ内で実行したいコマンド）
例 docker compose exec db mysql -u root -p

## 記憶領域のマウント
コンテナ内に置いたファイルが消えてしまわないように別の場所に保存する
### volumesについて
DockerEngineが管理している領域内にボリームを作成し、ディスクとしてコンテナにマウントする。
名前だけで管理できる反面、ボリュームに対して直接操作しづらいため、滅多に触らないか消してはいけない物を置く