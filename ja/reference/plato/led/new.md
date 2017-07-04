# singleton method Plato::LED.new

## new(pin, pullup=false, act=:low) -> LED

指定したPINに割り付けられたLEDのオブジェクトを生成して返します。

|引数||
|:--|:--|
|pin|LEDのPINを指定します。PINに指定できる値は使用するマイコンボード毎に異なります。|
|pullup|**true**を指定すると、ポートに内蔵されたプルアップ抵抗を有効にします。内蔵プルアップ抵抗が使用できるかどうかは使用するマイコンボード毎に異なります。|
|act|**:low**を指定するとLOWアクティブ(電圧が低いときが1、高いときが0)、**:high**を指定するとHIGHアクティブ(電圧が高いときが1、低いときが0)のポートに接続されたLEDと見なします。|

|戻り値||
|:--|:--|
|LED|生成したLEDオブジェクト|

### 例:
```Ruby
led = Plato::LED.new(0)
led.on      # 0番PINに接続されたLEDを点灯します
led.off     #                 LEDを消灯します
```
