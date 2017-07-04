# instance method PlatoDevice::XBee#flush

## flush -> nil

XBee通信モジュールの送信バッファをフラッシュします。  

|引数|
|:--|
|なし|

|戻り値|
|:--|
|なし|

### 例:
```Ruby
xb = PlatoDevice::XBee.open   # XBee通信モジュールをオープンします
"Hello, Plato!\n".each_byte do |dt|
  xb._write(dt)     # XBeeに1バイトずつデータを出力します
end
xb.flush            # フラッシュして送信完了を待ちます
```
