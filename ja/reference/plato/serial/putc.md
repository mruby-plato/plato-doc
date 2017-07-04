# instance method Plato::Serial#putc

## putc(data) -> nil

シリアルI/Fデバイスに1文字を出力します。  

|引数||
|:--|:--|
|data|シリアルI/Fデバイスに書き込む文字を指定します。2文字以上の文字列が渡された場合は先頭の1文字だけが書き込まれます。|

|戻り値|
|:--|
|なし|

### 例:
```Ruby
Plato::Serial.register_device(PlatoEnzi::Serial)    # enziボードのシリアルI/Fデバイスクラスを登録します
ser = Plato::Serial.open(9600, 8, 1, 1, :none)      # enziボードに接続されたシリアルI/Fデバイスをオープンします
ser.putc('A')   # シリアルI/Fデバイスに 'A' を出力します
"Plato".each_char do |c|
  ser.putc(c)   # シリアルI/Fデバイスに "Plato" の先頭から1文字ずつ出力します
end
```
