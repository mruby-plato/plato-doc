# instance method PlatoEnzi::I2C#write

## write(reg, data) -> nil

enziボードのI<sup>2</sup>Cデバイスに指定した値を出力します。  

|引数||
|:--|:--|
|reg|I<sup>2</sup>Cデバイスのレジスタ番号を指定します。指定できるレジスタ番号および取得できるデータの仕様はI<sup>2</sup>Cデバイスに依存します。|
|data|以下のいずれかの形式で出力する値を指定します。<li>数値(Fixnum)を指定した場合: 1バイトのデータとして出力します。<li>バイト配列(Array)を指定した場合: バイト配列の内容を順に出力します。<li>文字列(String)を指定した場合: 文字列を1文字(1バイト)ずつ出力します。<li>その他の形式を指定した場合: 文字列に変換し、1文字(1バイト)ずつ出力します。|

|戻り値|
|:--|
|nil|

### 例:
```Ruby
Plato::I2C.register_device(PlatoEnzi::I2C)  # enziボードのI2Cデバイスクラスを登録します
i2c = Plato::I2C.open(0b1000000)    # enziボードに接続されたI2Cデバイスをオープンします
i2c.write(0, 255)
i2c.write(0, [10, 20, 30])
i2c.write(0, "012")
i2c.write(0, :off)          # "off" が出力されます
```
