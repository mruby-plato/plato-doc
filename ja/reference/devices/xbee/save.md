# instance method PlatoDevice::XBee#save

## save -> nil

XBee通信モジュールの設定を内蔵フラッシュメモリに保存します。  
saveメソッド実行後はXBeeをリセットしても設定内容が保持されます。

|引数|
|:--|
|なし|

|戻り値|
|:--|
|nil|

### 例:
```Ruby
xb = PlatoDevice::XBee.open         # XBee通信モジュールをオープンします
xb.panid = '1234'                   # PAN IDを'1234'に変更します
xb.connect('0000000', '00000000')   # Coordinatorに接続します
xb.save     # 設定を保存します
```
