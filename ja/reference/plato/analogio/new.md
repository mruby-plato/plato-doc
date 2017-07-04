# singleton method Plato::AnalogIO.new

## new(pin, pullup=false, act=:low) -> AnalogIO

指定したPINに割り付けられたディジタルIOデバイスのオブジェクトを生成して返します。

|引数||
|:--|:--|
|pin|アナログIOのPINを指定します。PINに指定できる値は使用するマイコンボード毎に異なります。|

|戻り値||
|:--|:--|
|Plato::AnalogIO|生成したAnalogIOオブジェクト|

### 例:
```Ruby
io = Plato::AnalogIO.new(D8)
io.write(255)           # D8のPINに255を出力します
io1 = Plato::AnalogIO.new(A0)
p io1.read              # A0のPINからアナログ入力した値を表示します
```
