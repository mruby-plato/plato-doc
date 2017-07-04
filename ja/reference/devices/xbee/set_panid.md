# instance method PlatoDevice::XBee#panid=

## panid = id -> nil

XBee通信モジュールのPAN IDを設定します。  

|引数||
|:--|:--|
|id|PAN ID(ZigBeeネットワークの識別子)を指定します。<br>PAN IDには16進文字列4桁('0000'〜'FFFF')または16ビット数値(0〜0xFFFF)が指定できます。|

|戻り値|
|:--|
|なし|

### 例:
```Ruby
xb = PlatoDevice::XBee.open   # XBee通信モジュールをオープンします
xb.panid = '1234'             # PAN IDを設定します
[79, 75, 13].each do |dt|
  xb._write(dt)           # XBee通信モジュールに 79, 75, 13 の順に出力します
end
```
