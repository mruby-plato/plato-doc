# instance method Plato::Serial#getc

## getc -> String \| nil

シリアルI/Fデバイスから1バイトのデータを読み込み、文字データとして返します。  

|引数|
|:--|
|なし|

|戻り値||
|:--|:--|
|String \| nil|シリアルI/Fデバイスから読み込んだ1文字が返されます。受信データがない場合はnilが返されます。|

### 例:
```Ruby
Plato::Serial.register_device(PlatoEnzi::Serial)    # enziボードのシリアルI/Fデバイスクラスを登録します
ser = Plato::Serial.open(9600, 8, 1, 1, :none)      # enziボードに接続されたシリアルI/Fデバイスをオープンします
loop {
  c = ser.getc    # シリアルI/Fデバイスから1文字読み込みます
  print c if c    # 受信データがある場合は読み込んだ文字を表示します
}
```
