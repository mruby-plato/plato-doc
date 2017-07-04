# instance method PlatoDevice::XBee#reset

## reset -> nil

XBee通信モジュールのネットワーク設定をリセットします。  

|引数|
|:--|
|なし|

|戻り値|
|:--|
|nil|

### 例:
```Ruby
xb = PlatoDevice::XBee.open         # XBee通信モジュールをオープンします
xb.connect('00000000', '0000FFFF')  # ブロードキャスト接続します
#
xb.reset    # ネットワーク設定をリセットします
```
