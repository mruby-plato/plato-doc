# instance method PlatoDevice::XBee#my_address

## my_address -> Array

XBee通信モジュールのアドレスを取得します。  

|引数|
|:--|
|なし|

|戻り値||
|:--|:--|
|Array|XBee通信モジュールのアドレス(上位アドレス、下位アドレスの配列)が返されます。|

### 例:
```Ruby
xb = PlatoDevice::XBee.open     # XBee通信モジュールをオープンします
p xb.my_address     # -> ["0013A200", "D40C2092"]
```
