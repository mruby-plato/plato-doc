# instance method Plato::Serial#puts

## puts(*data) -> nil

シリアルI/Fデバイスに指定されたデータに改行を付加した文字列を出力します。  

|引数||
|:--|:--|
|data|シリアルI/Fデバイスに書き込むデータ列を指定します。データが文字列以外の場合は文字列に変換された後に出力されます。2つ以上のデータが渡された場合は渡された順に書き込まれます。|

|戻り値|
|:--|
|なし|

### 例:
```Ruby
Plato::Serial.register_device(PlatoEnzi::Serial)    # enziボードのシリアルI/Fデバイスクラスを登録します
ser = Plato::Serial.open(9600, 8, 1, 1, :none)      # enziボードに接続されたシリアルI/Fデバイスをオープンします
ser.puts('Plato')           # シリアルI/Fデバイスに "Plato\n" を出力します
ser.puts("ABC", 123, 0x20)  # シリアルI/Fデバイスに "ABC\n123\n32\n" を出力します
```
