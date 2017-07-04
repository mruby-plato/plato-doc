# singleton method PlatoDevice::XBee.open

## open(pan=nil) -> Plato::XBee

XBee通信モジュールをオープンし、XBeeデバイスクラスのインスタンスを返します。  

|引数||
|:--|:--|
|pan|PAN ID(ZigBeeネットワークの識別子)を指定します。<br>PAN IDには16進文字列4桁('0000'〜'FFFF')または16ビット数値(0〜0xFFFF)が指定できます。<br>nil(デフォルト)が指定された場合はXBeeに設定されているPAN IDが使用されます。|

|戻り値||
|:--|:--|
|Plato::XBee|XBeeデバイスクラスのインスタンス|

### 例:
```Ruby
xb = PlatoDevice::XBee.open('BEEF')     # XBee通信モジュールをオープンします
loop {
  dt = xb._read                 # XBeeから1バイト読み込みます
  if dt >= 0                    # データを受信した場合は
    print sprintf("%02X ", dt)  # 受信データを16進表示します
  end
}
```
