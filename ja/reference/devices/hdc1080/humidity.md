# instance method PlatoDevice::HDC1080#humidity

## humidity -> Float

温湿度センサHDC1080から読み込んだ湿度値(%)を返します。

|引数|
|:--|
|なし|

|戻り値||
|:--|:--|
|Float|HDC1080から読み込んだ湿度|

### 例:
```Ruby
hdc = Plato::HDC1080.new
p hdc.humidity      # -> 54.271
```
