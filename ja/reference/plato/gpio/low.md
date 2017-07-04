# instance method Plato::GPIO#low

## low -> Fixnum

GPIO(汎用IO)にLOWを出力します。

|引数||
|:--|:--|
|pin|GPIOのPINを指定します。PINに指定できる値は使用するマイコンボード毎に異なります。|

|戻り値||
|:--|:--|
|Fixnum|出力値(Plato::LOW)が返されます。|

### 例:
```Ruby
io = Plato::GPIO.new(0)
io.low              # 0番PINにLOWを出力します
```
