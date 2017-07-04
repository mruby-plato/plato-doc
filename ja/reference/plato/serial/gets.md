# instance method Plato::Serial#gets

## gets(rs="\n") -> String \| nil<br>gets(limit) -> String \| nil<br>gets(rs, limit) -> String \| nil

シリアルI/Fデバイスから1行のデータを読み込み、文字データとして返します。  

|引数||
|:--|:--|
|rs="\n"|行の区切り文字を指定します。<br>rsを受信するまでまたは受信データがなくなるまでを1行と見なします。|
|limit|最大読み込み文字数(バイト数)を指定します。|

|戻り値||
|:--|:--|
|String \| nil|シリアルI/Fデバイスから読み込んだ1行の文字列が返されます。区切り文字を読み込んだ場合は終端に区切り文字が付加されます。受信データがない場合はnilが返されます。|

### 例:
```Ruby
Plato::Serial.register_device(PlatoEnzi::Serial)    # enziボードのシリアルI/Fデバイスクラスを登録します
ser = Plato::Serial.open(9600, 8, 1, 1, :none)      # enziボードに接続されたシリアルI/Fデバイスをオープンします
loop {
  until s = ser.gets          # シリアルI/Fデバイスから1行読み込みます
    Plato::Machine.delay(10)
  end
  print s     # 読み込んだ文字列を表示します
  end
}
```
