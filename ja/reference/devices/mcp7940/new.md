# singleton method PlatoDevice::MCP7940.new

## new(addr=I2CADDR) -> PlatoDevice::MCP7940

MCP7940 RTCデバイスのオブジェクトを生成して返します。  

|引数||
|:--|:--|
|addr|MVP7940のI2Cアドレス(デフォルト:I2CADDR)を指定します。|

|戻り値||
|:--|:--|
|PlatoDevice::MCP7940|生成したMCP7940オブジェクトを返します。|

### 例:
```Ruby
rtc = PlatoDevice::MCP7940.new
p rtc.get_time  # -> [2017, 1, 27, 11, 18, 0]
```
