# instance method PlatoEnzi::Serial#_write

## _write(data) -> nil

enziボードのシリアルI/F(UART)デバイスに1バイトのデータを書き込みます。  

|引数||
|:--|:--|
|data|シリアルI/Fデバイスに書き込むバイトデータ(0〜255の数値)を指定します。|

|戻り値|
|:--|
|なし|

### 例:
```Ruby
Plato::Serial.register_device(PlatoEnzi::Serial)    # enziボードのシリアルI/Fデバイスクラスを登録します
ser = Plato::Serial.open(9600, 8, 1, 1, :none)      # enziボードに接続されたシリアルI/Fデバイスをオープンします
[79, 75, 13].each do |dt|
  ser._write(dt)            # シリアルI/Fデバイスに 79, 75, 13 の順に出力します
end
```
