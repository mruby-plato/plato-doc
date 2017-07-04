# instance method Plato::GPIO#high?

## high? -> true | false

GPIO(汎用IO)がHIGHレベルかどうかを判定した結果を返します。

|引数|
|:--|
|なし|

|戻り値||
|:--|:--|
|true \| false|GPIOデバイスがHIGHレベルの場合は**true**、LOWレベルの場合は**false**を返します。|

### 例:
```Ruby
io = Plato::GPIO.new(0)
p io.high?          # => true | false
```
