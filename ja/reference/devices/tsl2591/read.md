# instance method PlatoDevice::TSL2591#read

## read -> Array

照度センサTSL2591から読み込んだ照度(lux)を返します。

|引数|
|:--|
|なし|

|戻り値||
|:--|:--|
|Float|TSL2591から読み込んだ照度(lux)|

### 例:
```Ruby
tsl = Plato::TSL2591.new
p tsl.read      # -> 381.353
```
