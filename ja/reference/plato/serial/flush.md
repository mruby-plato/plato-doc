# instance method Plato::Serial#flush

## flush -> nil

シリアルI/Fの送信バッファをフラッシュします。  

|引数|
|:--|
|なし|

|戻り値|
|:--|
|なし|

### 例:
```Ruby
Plato::Serial.register_device(PlatoEnzi::Serial)    # enziボードのシリアルI/Fデバイスクラスを登録します
ser = Plato::Serial.open(9600, 8, 1, 1, :none)      # enziボードに接続されたシリアルI/Fデバイスをオープンします
"Hello, Plato!\n".each_byte do |dt|
  ser._write(dt)    # シリアルI/Fデバイスに1バイトずつデータを出力します
end
ser.flush           # フラッシュして送信完了を待ちます
```
