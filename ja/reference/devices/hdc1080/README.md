# class PlatoDevice::HDC1080

### クラスの継承リスト: PlatoDevice::HDC1080 < [Plato::Sensor](../../plato/sensor/README.md) < Object

## 要約

温湿度センサ(HDC1080)のデバイスクラスです。

## 定数

|定義|説明|
|:--|:--|
|I2CADDR|White TigerボードのHDC1080のI2Cアドレス(0b1000000)|

## 特異メソッド

|定義|説明|
|:--|:--|
|[new(addr=I2CADDR, ndigits=3, unit=:C) -> PlatoDevice::HDC1080](new.md)|HDC1080センサデバイスのオブジェクトを生成して返します。|

## インスタンスメソッド

|定義|説明|
|:--|:--|
|[temperature(unit=nil) -> Float](temperature.md)|HDC1080から読み込んだ温度値を返します。|
|[humidity -> Float](humidity.md)|HDC1080から読み込んだ湿度値(%)を返します。|
|[read -> Array](read.md)|HDC1080から読み込んだ温度、湿度を配列で返します。|
|[unit = u -> nil](setunit.md)|温度の取得単位を指定します。|
