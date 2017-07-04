# instance method PlatoEnzi::Serial#_read

## _read -> Fixnum

enziボードのシリアルI/F(UART)デバイスから1バイトのデータを読み込みます。  

|引数|
|:--|
|なし|

|戻り値||
|:--|:--|
|Fixnum|シリアルI/Fデバイスから読み込んだデータ(0〜255)が返されます。受信データがない場合は-1が返されます。|

### 例:
```Ruby
Plato::Serial.register_device(PlatoEnzi::Serial)    # enziボードのシリアルI/Fデバイスクラスを登録します
ser = Plato::Serial.open(9600, 8, 1, 1, :none)      # enziボードに接続されたシリアルI/Fデバイスをオープンします
loop {
  dt = ser._read                # シリアルI/Fデバイスから1バイト読み込みます
  if dt >= 0                    # データを受信した場合は
    print sprintf("%02X ", dt)  # 受信データを16進表示します
  end
}
```
