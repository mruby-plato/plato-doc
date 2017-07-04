# class PlatoDevice::TSL2591

### クラスの継承リスト: PlatoDevice::TSL2591 < [Plato::Sensor](../../plato/sensor/README.md) < Object

## 要約

照度センサ(TSL2591)のデバイスクラスです。

## 定数

|定義|説明|
|:--|:--|
|I2CADDR|White TigerボードのTSL2591のI2Cアドレス(0x29)|

## 特異メソッド

|定義|説明|
|:--|:--|
|[new(addr=I2CADDR, ndigits=3) -> PlatoDevice::TSL2591](new.md)|TSL2591センサデバイスのオブジェクトを生成して返します。|

## インスタンスメソッド

|定義|説明|
|:--|:--|
|[read -> Array](read.md)|TSL2591から読み込んだ照度(lux)を返します。|
|[gain = g -> nil](set_gain.md)|TSL2591のゲインを設定します。|
|[timing = t -> nil](set_timing.md)|TSL2591のインテグレーション時間を設定します。|
