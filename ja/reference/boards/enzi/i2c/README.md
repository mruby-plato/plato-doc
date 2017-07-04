# class Plato::I2C

### クラスの継承リスト: PlatoEnzi::I2C < [Plato::I2C](../../../plato/i2c/README.md) < Object

## 要約

enziボードでI<sup>2</sup>C(Inter-Integrated Circuit) I/Fへの入出力を行うためのクラスです。  

## 特異メソッド

|定義|説明|
|:--|:--|
|[new(addr, wait=10) -> PlatoEnzi::I2C](new.md)|I<sup>2</sup>Cデバイスのオブジェクトを生成して返します。|

## インスタンスメソッド

|定義|説明|
|:--|:--|
|[read(reg, len, type=:as_array) -> Array \| String](read.md)|I<sup>2</sup>Cデバイスから読み込んだデータを返します。|
|[write(reg, data) -> nil](write.md)|I<sup>2</sup>Cデバイスにデータを出力します。|
