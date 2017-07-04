# instance method PlatoDevice::XBee#close

## close -> nil

XBee通信モジュールをクローズします。  

|引数|
|:--|
|なし|

|戻り値|
|:--|
|なし|

### 例:
```Ruby
xb = PlatoDevice::XBee.open   # XBee通信モジュールをオープンします
[79, 75, 13].each do |dt|
  xb._write(dt)           # XBee通信モジュールに 79, 75, 13 の順に出力します
end
xb.close            # XBee通信モジュールをクローズします
```
