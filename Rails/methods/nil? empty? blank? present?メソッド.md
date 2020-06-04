## Rubyの標準メソッド・Railsへの拡張メソッド  

「Ruby標準」: Ruby標準メソッド
「Rails拡張」: Railsへの拡張メソッド、Rubyでは使えない

|Ruby標準|Rails拡張|
| :---: | :---: | 
| nil?| blank? |
| empty? | present? |

### Rails拡張メソッドblank?/present?はRuby標準メソッドの組み合わせ

・blank? ~ nil? + empty?  
・present? ~ !blank?  
のような感じ。

https://railsdoc.com/active_support
