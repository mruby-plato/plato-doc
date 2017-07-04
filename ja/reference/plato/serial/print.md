# instance method Plato::Serial#print

## print(*data) -> nil

シリアルI/Fデバイスに指定されたデータを文字列として出力します。  
[puts](puts.md)のように行の区切り文字は出力されません。

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
ser.puts('Plato')           # シリアルI/Fデバイスに "Plato" を出力します
ser.puts("ABC", 123, 0x20)  # シリアルI/Fデバイスに "ABC12332" を出力します
```
