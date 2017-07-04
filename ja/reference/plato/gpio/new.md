# singleton method Plato::GPIO.new

## new(pin) -> GPIO

指定したPINに割り付けられたGPIO(汎用IO)デバイスのオブジェクトを生成して返します。

|引数||
|:--|:--|
|pin|GPIOのPINを指定します。PINに指定できる値は使用するマイコンボード毎に異なります。|

|戻り値||
|:--|:--|
|GPIO|生成したGPIOオブジェクト|

### 例:
```Ruby
io = Plato::GPIO.new(0)
io.high             # 0番PINにHIGHを出力します
```
