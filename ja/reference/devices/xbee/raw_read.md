# instance method PlatoDevice::XBee#_read

## _read -> Fixnum

XBee通信モジュールから1バイトのデータを読み込みます。  

|引数|
|:--|
|なし|

|戻り値||
|:--|:--|
|Fixnum|XBeeから読み込んだデータ(0〜255)が返されます。受信データがない場合は-1が返されます。|

### 例:
```Ruby
xb = PlatoDevice::XBee.open     # XBee通信モジュールをオープンします
loop {
  dt = xb._read                 # XBeeから1バイト読み込みます
  if dt >= 0                    # データを受信した場合は
    print sprintf("%02X ", dt)  # 受信データを16進表示します
  end
}
```
