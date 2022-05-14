# docker_rails_mysql
DockerでRails×MySQLの環境を構築する。

## 環境(適宜変更する)
* Ruby:   3系
* Rails:  最新
* MySQL:  8.0

## 手順
1. `git clone https://github.com/hojoko/docker_rails_mysql.git`
2. `rm -rf .git`
3. `mv docker_rails_mysql 任意のアプリ名`
4. `docker-compose run web rails new . --force --database=mysql --skip-test`
5. `docker-compose build`
6. `config/database.yml`の`password`と`host`を編集
7. `docker-compose run web rails db:create`
8. `docker-compose up -d`
9. `docker-compose exec web rails s`でサーバーが起動しているか確認
10. `git init`
