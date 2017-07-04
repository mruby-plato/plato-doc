# singleton method PlatoDevice::TSL2591.new

## new(addr=I2CADDR, ndigits=3) -> PlatoDevice::TSL2591

TSL2591センサデバイスのオブジェクトを生成して返します。

|引数||
|:--|:--|
|addr|TSL2591のI2Cアドレス(デフォルト:I2CADDR)を指定します。|
|ndigits|読み取り値を丸める小数点以下の桁数を指定します。デフォルトでは小数点以下3桁に丸められます。|

|戻り値||
|:--|:--|
|PlatoDevice::TSL2591|生成したTSL2591オブジェクトを返します。|

### 例:
```Ruby
tsl = PlatoDevice::TSL2591.new
p tsl.read      # -> 381.353
```
