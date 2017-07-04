# instance method Plato::GPIO#high

## high -> Fixnum

GPIO(汎用IO)にHIGHを出力します。

|引数||
|:--|:--|
|pin|GPIOのPINを指定します。PINに指定できる値は使用するマイコンボード毎に異なります。|

|戻り値||
|:--|:--|
|Fixnum|出力値(Plato::HIGH)が返されます。|

### 例:
```Ruby
io = Plato::GPIO.new(0)
io.high             # 0番PINにHIGHを出力します
```
