# instance method Plato::Serial#term_char=

## term_char = cr -> nil

入出力の区切り文字(行の終端文字)を指定します。  
区切り文字が指定されない場合は、"\n"がデフォルトの区切り文字として使用されます。

|引数||
|:--|:--|
|cr|区切り文字を指定します。|

|戻り値|
|:--|
|なし|

### 例:
```Ruby
Plato::Serial.register_device(PlatoEnzi::Serial)    # enziボードのシリアルI/Fデバイスクラスを登録します
ser = Plato::Serial.open(9600, 8, 1, 1, :none)      # enziボードに接続されたシリアルI/Fデバイスをオープンします
ser.term_char = "\r"    # "\r"(CR)を区切り文字に指定します
s = ser.gets            # 終端"\r"の1行の文字列を読み込みます
```
