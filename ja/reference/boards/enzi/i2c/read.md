# instance method PlatoEnzi::I2C#read

## read(reg, len, type=:as_array) -> Array \| String

enziボードのI<sup>2</sup>Cデバイスから値を読み込みます。  

|引数||
|:--|:--|
|reg|I<sup>2</sup>Cデバイスのレジスタ番号を指定します。指定できるレジスタ番号および取得できるデータの仕様はI<sup>2</sup>Cデバイスに依存します。|
|len|読み込むデータのサイズ(バイト数)を指定します。|
|type|戻り値のデータ形式を **:as_array** または **:as_string** で指定します。<li>**:as_array** (デフォルト) が指定された場合: バイト配列(数値の配列)が返されます。<li>**:as_string** が指定された場合: Stringの形式で返されます。|

|戻り値||
|:--|:--|
|Array \| String|I<sup>2</sup>Cデバイスから読み込んだデータがArrayまたはStringの形式で返されます。|

### 例:
```Ruby
Plato::I2C.register_device(PlatoEnzi::I2C)  # enziボードのI2Cデバイスクラスを登録します
i2c = Plato::I2C.open(0b1000000)    # enziボードに接続されたI2Cデバイスをオープンします
t = i2c.read(0, 2)              # -> [100, 22]
h = i2c.read(0, 2, :as_string)  # -> "d\026"
```
