# instance method Plato::I2C#write

## write(reg, data) -> nil

I<sup>2</sup>Cデバイスに指定した値を出力するための雛形のメソッドです。  
実際のI<sup>2</sup>Cデバイスへの出力はI2Cモジュールをincludeしたデバイスクラス側で行われます。

|引数||
|:--|:--|
|reg|I<sup>2</sup>Cデバイスのレジスタ番号を指定します。指定できるレジスタ番号および取得できるデータの仕様はI<sup>2</sup>Cデバイスに依存します。|
|data|出力する値を指定します。値の内容はサブクラスに実装されたwriteメソッドに依存します。|

|戻り値|
|:--|
|nil|

### 例:
```Ruby
Plato::I2C.register_device(PlatoEnzi::I2C)  # enziボードのI2Cデバイスクラスを登録します
i2c = Plato::I2C.open(0b1000000)    # enziボードに接続されたI2Cデバイスをオープンします
i2c.write(0, "012")
```
