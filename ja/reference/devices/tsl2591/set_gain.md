# instance method PlatoDevice::TSL2591#gain=

## gain = g -> nil

照度センサ(TSL2591)のゲインを設定します。  

|引数||
|:--|:--|
|g|ゲインを指定します。<li>:low (1 lux)<li>:medium (25 lux: デフォルト)<li>:high (428 lux)<li>:max (9876 lux)|

|戻り値|
|:--|
|nil|

### 例:
```Ruby
tsl = PlatoDevice::TSL2591.new          # 照度センサデバイスのオブジェクトを生成します
tsl.gain = :low
p tsl.read          # -> 308.253
```
