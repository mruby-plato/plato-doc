# instance method PlatoDevice::HDC1080#temperature

## temperature(unit=nil) -> Float

温湿度センサHDC1080から読み込んだ温度値を返します。

|引数||
|:--|:--|
|unit=nil|温度の単位を指定します。**:C**が指定された場合は摂氏温度、**:F**が指定された場合は華氏温度で取得されます。**nil**(デフォルト)が指定された場合は[PlatoDevice::HDC1080.new](new.md)の引数**unit**またはPlatoDevice::HDC1080#unit=で指定された単位で取得されます。|

|戻り値||
|:--|:--|
|Float|HDC1080から読み込んだ温度|

### 例:
```Ruby
hdc = Plato::HDC1080.new
p hdc.temperature       # -> 27.124
p hdc.temperature(:F)   # -> 80.823
```
