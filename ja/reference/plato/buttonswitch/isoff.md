# instance method Plato::ButtonSwitch#off?

## off? -> true | false

ボタンスイッチがOFF状態かを判定した結果を返します。

|引数|
|:--|
|なし|

|戻り値||
|:--|:--|
|true \| false|ボタンスイッチがOFFの場合は**true**、ONの場合は**false**を返します。|

### 例:
```Ruby
btn = Plato::ButtonSwitch.new(0)
p btn.off?      # => true | false
```
