# singleton method Plato::I2C.register_device

## register_device(device) -> Object

I<sup>2</sup>Cデバイスクラスを登録します。  
PlatoIDEで生成したアプリケーションでは使用するマイコンボード用のマシンデバイスクラスが自動登録されるため、本メソッドを使用する必要はありません。

|引数||
|:--|:--|
|device|マイコンボードに依存するI<sup>2</sup>C入出力を行うI<sup>2</sup>Cデバイスクラスを指定します。指定するI<sup>2</sup>Cデバイスクラスは[read](read.md)メソッドおよび[write](write.md)メソッドを含む必要があります。|

|戻り値||
|:--|:--|
|Object|登録したI<sup>2</sup>Cデバイスクラス|

### 例:
```Ruby
Plato::I2C.register_device(PlatoEnzi::I2C)  # enziボードのI2Cデバイスクラスを登録します
i2c = Plato::I2C.open(0b1000000)    # enziボードに接続されたI2Cデバイスをオープンします
```
