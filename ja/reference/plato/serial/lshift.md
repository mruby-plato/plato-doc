# instance method Plato::Serial#<<

## self \<\< data -> self

シリアルI/Fデバイスにデータを書き込みます。  

|引数||
|:--|:--|
|data|シリアルI/Fデバイスに書き込むデータを指定します。<br>文字列に変換された結果が書き込まれます。|

|戻り値||
|:--|:--|
|self|レシーバのインスタンスが返されます。|

### 例:
```Ruby
Plato::Serial.register_device(PlatoEnzi::Serial)    # enziボードのシリアルI/Fデバイスクラスを登録します
ser = Plato::Serial.open(9600, 8, 1, 1, :none)      # enziボードに接続されたシリアルI/Fデバイスをオープンします
ser << "Plato"          # シリアルI/Fデバイスに 80,108,97,116,111 ("Plato"の文字コード) の順に出力します
ser << 3                # シリアルI/Fデバイスに "3" を出力します
ser << 1 << 2 << "\r"   # シリアルI/Fデバイスに "12\n" を出力します
```
