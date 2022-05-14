# docker_rails_mysql
DockerでRails×MySQLの環境を構築する。

## 環境(適宜変更する)
* Ruby:   3系
* Rails:  最新
* MySQL:  8.0

## 手順
1. `git clone https://github.com/hojoko/docker_rails_mysql.git`
2. `rm -rf docker_rails_mysql/.git`
3. `mv docker_rails_mysql 任意のアプリ名`
4. `cd 任意のアプリ名`
5. `docker-compose run web rails new . --force --database=mysql --skip-test`
6. `docker-compose build`
7. `config/database.yml`の`password`と`host`を編集
8. `docker-compose run web rails db:create`
9. `docker-compose down`
10. `docker-compose up -d`
11. `localhost:3000`で確認
12. `.gitignore`に`/db/mysql_data`を追加
13. GitHubのリポジトリを追加
