# instance method Plato::ButtonSwitch#on?

## on? -> true | false

ボタンスイッチがON状態かを判定した結果を返します。

|引数|
|:--|
|なし|

|戻り値||
|:--|:--|
|true \| false|ボタンスイッチがONの場合は**true**、OFFの場合は**false**を返します。|

### 例:
```Ruby
btn = Plato::ButtonSwitch.new(0)
p btn.on?       # => true | false
```
