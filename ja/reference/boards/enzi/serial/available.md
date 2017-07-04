# instance method PlatoEnzi::Serial#available

## available -> Fixnum

enziボードのシリアルI/F(UART)デバイスに受信しているデータ長を返します。  

|引数|
|:--|
|なし|

|戻り値||
|:--|:--|
|Fixnum|シリアルI/Fデバイスに受信しているデータ長が返されます。受信データがない場合は0が返されます。|

### 例:
```Ruby
Plato::Serial.register_device(PlatoEnzi::Serial)    # enziボードのシリアルI/Fデバイスクラスを登録します
ser = Plato::Serial.open(9600, 8, 1, 1, :none)      # enziボードに接続されたシリアルI/Fデバイスをオープンします
loop {
  while ser.available == 0            # シリアルI/Fデバイスからデータを受信するまで
    Plato::Machine.delay(10)          # 10ミリ秒待ちます
  end
  print sprintf("%02X ", ser._read)   # 受信データを16進表示します
}
```
