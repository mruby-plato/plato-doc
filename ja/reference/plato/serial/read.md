# instance method Plato::Serial#read

## read(len=nil, type=:as_array, tmo=2000) -> Array \| String

シリアルI/Fデバイスから読み込んだデータを返します。  

|引数||
|:--|:--|
|len=nil|読み込むデータの最大サイズ(バイト数)を指定します。シリアルI/Fデバイスが受信しているデータ長がlenより短い場合は受信待ちは行わず、受信しているデータを返します。**nil**(デフォルト)が指定された場合はシリアルI/Fデバイスが受信しているデータを全て読み込みます。|
|type=:as_array|戻り値のデータ形式を指定します。**:as_array**(デフォルト)が指定された場合はバイト配列(数値の配列)、**:as_string**が指定された場合はStringの形式で返されます。|
|tmo=2000|データ受信のための最大待ち時間をミリ秒単位で指定します。|

|戻り値||
|:--|:--|
|Array \| String|シリアルI/Fデバイスから読み込んだデータがArrayまたはStringの形式で返されます。読み込んだデータがない場合は空の配列または文字列が返されます。|

### 例:
```Ruby
Plato::Serial.register_device(PlatoEnzi::Serial)    # enziボードのシリアルI/Fデバイスクラスを登録します
ser = Plato::Serial.open(9600, 8, 1, 1, :none)      # enziボードに接続されたシリアルI/Fデバイスをオープンします
loop {
  while ser.available < 10
    Plato::Machine.delay(10)
  end
  da = ser.read(2)                      # シリアルI/Fデバイスから2バイト読み込み、配列で取得します
  ds = ser.read(8, :as_string)          # シリアルI/Fデバイスから8バイト読み込み、文字列で取得します
  ds = ser.read(nil, :as_array, 10000)  # シリアルI/Fデバイスから10秒間の間に受信したデータを配列で取得します
}
```
