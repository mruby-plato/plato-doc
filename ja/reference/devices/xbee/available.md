# instance method PlatoDevice::XBee#available

## available -> Fixnum

XBee通信モジュールに受信しているデータ長を返します。  

|引数|
|:--|
|なし|

|戻り値||
|:--|:--|
|Fixnum|XBee通信モジュールに受信しているデータ長が返されます。受信データがない場合は0が返されます。|

### 例:
```Ruby
xb = PlatoDevice::XBee.open           # XBee通信モジュールをオープンします
loop {
  while xb.available == 0             # XBeeからデータを受信するまで
    Plato::Machine.delay(10)          # 10ミリ秒待ちます
  end
  print sprintf("%02X ", xb._read)    # 受信データを16進表示します
}
```
