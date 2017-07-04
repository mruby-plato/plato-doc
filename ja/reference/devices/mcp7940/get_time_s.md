# singleton method PlatoDevice::MCP7940.get_time

## get_time -> Array

RTCデバイス(MCP7940)から時刻を取得します。  
処理内容はインスタンスメソッドの[get_time](get_time.md)を呼び出した場合と同じです。

|引数|
|:--|
|なし|

|戻り値||
|:--|:--|
|Array|現在時刻を [year, month, day, hour, minute, second] の形式で返します。|

### 例:
```Ruby
p PlatoDevice::MCP7940.get_time     # -> [2017, 1, 27, 11, 18, 0]
```
