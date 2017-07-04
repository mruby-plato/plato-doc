# instance method PlatoDevice::XBee#_write

## _write(data) -> nil

XBee通信モジュールに1バイトのデータを書き込みます。  

|引数||
|:--|:--|
|data|XBee通信モジュールに書き込むバイトデータ(0〜255の数値)を指定します。|

|戻り値|
|:--|
|なし|

### 例:
```Ruby
xb = PlatoDevice::XBee.open # XBee通信モジュールをオープンします
[79, 75, 13].each do |dt|
  xb._write(dt)             # XBee通信モジュールに 79, 75, 13 の順に出力します
end
```
