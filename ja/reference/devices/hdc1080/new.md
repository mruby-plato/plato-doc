# singleton method PlatoDevice::HDC1080.new

## new(addr=I2CADDR, ndigits=3, unit=:C) -> PlatoDevice::HDC1080

HDC1080センサデバイスのオブジェクトを生成して返します。

|引数||
|:--|:--|
|addr|HDC1080のI2Cアドレス(デフォルト:I2CADDR)を指定します。|
|ndigits|読み取り値を丸める小数点以下の桁数を指定します。デフォルトでは小数点以下3桁に丸められます。|
|unit|温度の単位を指定します。**:C**が指定された場合は摂氏温度、**:F**が指定された場合は華氏温度で取得されます。|

|戻り値||
|:--|:--|
|PlatoDevice::HDC1080|生成したHDC1080オブジェクトを返します。|

### 例:
```Ruby
hdc1 = PlatoDevice::HDC1080.new
p hdc1.read     # -> "[27.124, 54.275]"
hdc2 = PlatoDevice::HDC1080.new(PlatoDevice::HDC1080::I2CADDR, 2, :F)
p hdc2.read     # -> "[80.82, 54.28]"
```
