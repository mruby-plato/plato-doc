# instance method PlatoDevice::HDC1080#unit=

## unit = u -> nil

温度の取得単位を指定します。

|引数||
|:--|:--|
|u|温度の取得単位を **:C** (摂氏温度) または **:F** (華氏温度) で指定します。|

|戻り値|
|:--|
|なし|

### 例:
```Ruby
hdc = Plato::HDC1080.new
hdc.unit = :F   # => nil
```
