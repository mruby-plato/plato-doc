# module Plato::I2C

### モジュールの継承リスト: Plato::I2C

## 要約

I<sup>2</sup>C(Inter-Integrated Circuit)シリアルI/Fへの入出力操作を定義したモジュールです。  

## 特異メソッド

|定義|説明|
|:--|:--|
|[register_device(device) -> Object](register_device.md)|I<sup>2</sup>Cデバイスを登録します。|
|[open(addr) -> Object](open.md)|I<sup>2</sup>Cデバイスをオープンし、I<sup>2</sup>Cデバイスクラスのインスタンスを返します。|

## インスタンスメソッド

|定義|説明|
|:--|:--|
|[read(reg, len, type=:as_array) -> Array \| String](read.md)|I<sup>2</sup>Cデバイスから読み込んだデータを返します。|
|[write(reg, data) -> nil](write.md)|I<sup>2</sup>Cデバイスにデータを出力します。|
