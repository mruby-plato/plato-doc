# instance method PlatoDevice::HDC1080#read

## read -> Array

温湿度センサHDC1080から読み込んだ温度、湿度を配列で返します。

|引数|
|:--|
|なし|

|戻り値||
|:--|:--|
|Array|HDC1080から読み込んだ温度・湿度 [温度, 湿度]|

### 例:
```Ruby
hdc = Plato::HDC1080.new
p hdc.read      # -> "[27.124, 54.271]"
```
