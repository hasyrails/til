## rails db でデータベースを起動

```
$ rails db
```
でdatabase.yml　で設定したデータベースが起動される。

### database.yml
```$ rails db```でsqlite3を起動する場合のdatabase.yml↓
```
development:
  <<: *default
  database: db/development.sqlite3

# Warning: The database defined as "test" will be erased and
# re-generated from your development database when you run "rake".
# Do not set this db to the same as development or production.
test:
  <<: *default
  database: db/test.sqlite3

production:
  <<: *default
  database: db/production.sqlite3

```
