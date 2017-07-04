# instance method PlatoDevice::XBee#connections

## connections -> Array

ペアリングされたZigBeeデバイスのアドレスを取得します。  

|引数|
|:--|
|なし|

|戻り値||
|:--|:--|
|Array|ペアリングされたZigBeeデバイスのアドレス(上位アドレス、下位アドレスの配列)の一覧を配列で取得します。<br>ペアリングされたZigBeeデバイスがない場合は空の配列が返されます。|

### 例:
```Ruby
xb = PlatoDevice::XBee.open     # XBee通信モジュールをオープンします
p xb.connections                # -> []  (ペアリングデバイスなし)
Plato::Machine.delay(10000)     # 10秒待つ
p xb.connections                # -> [['0013A200', '45C68A4F'], ['0013A200', 'A0042D920']] (2つのデバイスとペアリングされた)
```
