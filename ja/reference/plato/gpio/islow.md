# instance method Plato::GPIO#low?

## low? -> true | false

GPIO(汎用IO)がLOWレベルかどうかを判定した結果を返します。

|引数|
|:--|
|なし|

|戻り値||
|:--|:--|
|true \| false|GPIOデバイスがLOWレベルの場合は**true**、HIGHレベルの場合は**false**を返します。|

### 例:
```Ruby
io = Plato::GPIO.new(0)
p io.low?           # => true | false
```
