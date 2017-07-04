# instance method PlatoDevice::XBee#panid

## panid -> String

XBee通信モジュールに設定されているPAN IDを取得します。  

|引数|
|:--|
|なし|

|戻り値||
|:--|:--|
|String|XBee通信モジュールに設定されているPAN ID(16進文字列4桁)が返されます。|

### 例:
```Ruby
xb = PlatoDevice::XBee.open     # XBee通信モジュールをオープンします
p xb.panid      # -> "BEEF"
xb.panid = 0x1234
p xb.panid      # -> "1234"
```
