# docker_rails_mysql
DockerでRails×MySQLの環境を構築する。

## 環境(適宜変更する)
* Ruby:   3系
* Rails:  7系
* MySQL:  5.7

## 手順
### 1. このリポジトリをクローン
```
git clone https://github.com/hojoko/docker_rails_mysql.git`
```
### 2. git管理を削除
```
rm -rf docker_rails_mysql/.git
```
### 3. 任意のアプリ名を設定し移動
```
mv docker_rails_mysql 任意のアプリ名
```
```
cd 任意のアプリ名
```
### 4. dockerで環境構築 
```
docker-compose run web rails new . --force --database=mysql --no-deps --skip-test
```
```
docker-compose build
```
### 5. `config/database.yml`の`password`と`host`を編集
### 6. DBの作成 
```
docker-compose run web rails db:create
```
### 7. dockerの立ち上げ 
```
docker-compose down
```
```
docker-compose up -d
```
### 8. `localhost:3000`で確認
### 9. GitHubのリポジトリを追加
