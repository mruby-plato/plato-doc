# singleton method PlatoDevice::MCP7940.set_time

## set_time(time) -> nil

RTCデバイス(MCP7940)に時刻を設定します。  
処理内容はインスタンスメソッドの[set_time](set_time.md)を呼び出した場合と同じです。

|引数||
|:--|:--|
|time|現在時刻情報を指定します。<br>日時の形式は配列または文字列で指定します。<li>配列の場合: [year, month, day, hour, minute, second]<li>文字列の場合: 'yyyyMMddhhmmss'<br>時間(時分秒)が省略された場合には0が指定されたものとします。|

|戻り値|
|:--|
|nil|

### 例:
```Ruby
PlatoDevice::MCP7940.set_time('20170127111800')             # 2017/1/27 11:18:00
PlatoDevice::MCP7940.set_time('2017012711')                 # 2017/1/27 11:00:00
PlatoDevice::MCP7940.set_time([2017, 1, 27, 11, 18, 0])     # 2017/1/27 11:18:00
PlatoDevice::MCP7940.set_time([2017, 1, 27])                # 2017/1/27 00:00:00
```
