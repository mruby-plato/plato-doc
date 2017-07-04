# singleton method Plato::I2C.open

## open(addr) -> Object

I<sup>2</sup>Cデバイスをオープンし、I<sup>2</sup>Cデバイスクラスのインスタンスを返します。  

|引数||
|:--|:--|
|addr|操作対象のI<sup>2</sup>CデバイスのI<sup>2</sup>Cアドレスを指定します。|

|戻り値||
|:--|:--|
|Object|I<sup>2</sup>Cデバイスクラスのインスタンス|

### 例:
```Ruby
Plato::I2C.register_device(PlatoEnzi::I2C)  # enziボードのI2Cデバイスクラスを登録します
i2c = Plato::I2C.open(0b1000000)    # enziボードに接続されたI2Cデバイスをオープンします
```
