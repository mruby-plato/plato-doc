# singleton method PlatoEnzi::Serial.new

## new(baud, dbits=8, start=1 stop=1, parity=:none) -> PlatoEnzi::Serial

enziボードのシリアルI/F(UART)デバイスをオープンし、シリアルI/Fデバイスのインスタンスを返します。  
[Plato::Serial.open](../../serial/open.html)から呼び出されるため、本メソッドを直接利用する必要はありません。

|引数||
|:--|:--|
|baud|シリアル通信の転送速度(ボーレート)を指定します。enziボードでは以下の値が指定できます。<br>300, 600, 1200, 2400, 4800, 9600, 19200, 38400, 57600, 115200|
|dbits|シリアル通信データのバイト毎のビット長を指定します。デフォルトは8bitです。|
|start|シリアル通信データのバイト毎のスタートビット長を指定します。デフォルトは1bitです。|
|stop|シリアル通信データのバイト毎のストップビット長を指定します。デフォルトは1bitです。|
|parity|シリアル通信データのバイト毎のパリティチェック方式(パリティチェックなし(:none)、偶数パリティ(:even)、奇数パリティ(:odd)のいずれか)を指定します。デフォルトはバリティチェックなし(:none)です。|

|戻り値||
|:--|:--|
|PlatoEnzi::Serial|シリアルI/Fデバイスクラスのインスタンスが返されます。|

### 例:
```Ruby
Plato::Serial.register_device(PlatoEnzi::Serial)    # enziボードのシリアルI/Fデバイスクラスを登録します
ser = Plato::Serial.open(9600, 8, 1, 1, :none)      # enziボードに接続されたシリアルI/Fデバイスをオープンします
```
