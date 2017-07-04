# instance method Plato::Serial#write

## write(data) -> nil

シリアルI/Fデバイスにデータを書き込みます。  

|引数||
|:--|:--|
|data|シリアルI/Fデバイスに書き込むデータを指定します。<br>- 整数値(Fixnum)が渡された場合: ([_write](raw_write.md)と同じ動作)となり、1バイトの数値として書き込みます。<br>- 配列(Array)が指定された場合: バイト配列(0〜255の数値配列)の先頭から順に書き込みます。<br>- 文字列(String)が指定された場合: 先頭から1文字(1バイト)ずつ順に書き込みます。<br>- それ以外のデータが渡された場合: 文字列に変換された結果が書き込まれます。|

|戻り値|
|:--|
|なし|

### 例:
```Ruby
Plato::Serial.register_device(PlatoEnzi::Serial)    # enziボードのシリアルI/Fデバイスクラスを登録します
ser = Plato::Serial.open(9600, 8, 1, 1, :none)      # enziボードに接続されたシリアルI/Fデバイスをオープンします
ser.write(3)              # シリアルI/Fデバイスに 3 を出力します
ser.write([79, 75, 13])   # シリアルI/Fデバイスに 79,75,13 の順に出力します
ser.write("Plato")        # シリアルI/Fデバイスに 80,108,97,116,111 ("Plato"の文字コード) の順に出力します
```
