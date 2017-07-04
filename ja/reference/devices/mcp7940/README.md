# class PlatoDevice::MCP7940

### クラスの継承リスト: PlatoDevice::MCP7940 < [Plato::RTC](../../plato/rtc/README.md) < Object

## 要約

RTC(MCP7940)のデバイスクラスです。  

## 定数

|定義|説明|
|:--|:--|
|I2CADDR|White TigerボードのMCP7940のI2Cアドレス(0x6f)|

## 特異メソッド

|定義|説明|
|:--|:--|
|[new(addr=I2CADDR) -> PlatoDevice::MCP7940](new.md)|MCP7940 RTCデバイスのオブジェクトを生成して返します。|
|[set_time(time) -> nil](set_time_s.md)|RTCの時刻を設定します。|
|[get_time -> Array](get_time_s.md)|RTCから現在時刻を取得します。|

## インスタンスメソッド

|定義|説明|
|:--|:--|
|[set_time(time) -> nil](set_time.md)|RTCの時刻を設定します。|
|[get_time -> Array](get_time.md)|RTCから現在時刻を取得します。|
