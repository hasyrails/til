## 過去日・未来日判定の判定を行う

### 現在日付、現在時刻との比較コードは長い
設定した日付(例えば```release_date```)が過去日、未来日かどうかの判定を
```ruby
release_date > Date.today
```

```ruby
release_time > Datetime.now
```
のようにDate.todayと比較して条件として設定するのは長い

### ```past?```/```future?```を使うと簡潔

Date/Datetimeどちらにも対応している

```ruby
release_date.future?
```

```ruby
release_time.future?
```

https://madogiwa0124.hatenablog.com/entry/2018/01/08/175142
