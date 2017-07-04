# instance method Plato::ZigBee#connect

## connect(adrh, adrl) -> nil

ZigBeeネットワークに接続します。  
ZigBeeネットワークへの接続処理はデバイス毎に異なるため、実際の接続処理はZigBeeデバイス毎のサブクラスにて実施されます。

### ブロードキャスト通信を行う場合
- ZigBeeデバイスがCoordinatorの場合  
  adrh = '00000000', adrl = '0000FFFF' を指定します。
- ZigBeeデバイスがRouterまたはEndDeviceの場合  
  adrh = '00000000', adrl = '00000000' を指定します。

### 宛先指定通信を行う場合  
- 宛先のデバイスアドレスを adrh, adrl に指定します。

|引数||
|:--|:--|
|adrh|宛先アドレス(上位)を16進文字列8桁で指定します。|
|adrl|宛先アドレス(下位)を16進文字列8桁で指定します。|

|戻り値|
|:--|
|nil|

### 例:
このメソッドではZigBeeデバイスへの操作は行われないため、使用しても効果がありません。  
