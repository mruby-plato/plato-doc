# instance method PlatoDevice::TSL2591#timing=

## gain = g -> nil

照度センサ(TSL2591)のインテグレーション時間を設定します。  

|引数||
|:--|:--|
|g|インテグレーション時間を指定します。<li>:_100ms (100ms : デフォルト)<li>:_200ms (200ms)<li>:_300ms (300ms)<li>:_400ms (400ms)<li>:_500ms (500ms)<li>:_600ms (600ms)|

|戻り値|
|:--|
|nil|

### 例:
```Ruby
tsl = PlatoDevice::TSL2591.new          # 照度センサデバイスのオブジェクトを生成します
tsl.timing = :_200ms
p tsl.read          # -> 308.253
```
