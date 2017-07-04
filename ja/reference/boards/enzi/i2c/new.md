# singleton method PlatoEnzi::I2C.new

## new(addr, wait=10) -> PlatoEnzi::I2C

enziボードのI<sup>2</sup>Cデバイスをオープンし、I<sup>2</sup>Cデバイスのオブジェクトを返します。  
[Plato::I2C.open](../../../plato/i2c/open.html)から呼び出されるため、本メソッドを直接利用する必要はありません。

|引数||
|:--|:--|
|addr|操作対象のI<sup>2</sup>CデバイスのI<sup>2</sup>Cアドレスを指定します。|
|wait|ライブラリ内部で使用されるウェイト値です。デフォルト値(10)を設定して下さい。|

|戻り値||
|:--|:--|
|Object|I<sup>2</sup>Cデバイスクラスのインスタンスを返します。|

### 例:
```Ruby
Plato::I2C.register_device(PlatoEnzi::I2C)  # enziボードのI2Cデバイスクラスを登録します
i2c = Plato::I2C.open(0b1000000)    # enziボードに接続されたI2Cデバイスをオープンします
```
