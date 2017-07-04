# singleton method Plato::DigitalIO.new

## new(pin, pullup=false, act=:low) -> DigitalIO

指定したPINに割り付けられたディジタルIOデバイスのオブジェクトを生成して返します。

|引数||
|:--|:--|
|pin|ディジタルIOのPINを指定します。PINに指定できる値は使用するマイコンボード毎に異なります。|
|pullup|**true**を指定すると、ポートに内蔵されたプルアップ抵抗を有効にします。内蔵プルアップ抵抗が使用できるかどうかは使用するマイコンボード毎に異なります。|
|act|**:low**を指定するとLOWアクティブ(電圧が低いときが1、高いときが0)、**:high**を指定するとHIGHアクティブ(電圧が高いときが1、低いときが0)のディジタルポートと見なします。|

|戻り値||
|:--|:--|
|DigitalIO|生成したDigitalIOオブジェクト|

### 例:
```Ruby
io = Plato::DigitalIO.new(0)
io.high             # 0番PINにHIGHを出力します
io1 = Plato::DigitalIO.new(1, true, :high)
p io1.low?          # 1番PINがLOWレベルかの判定結果を表示します
```
