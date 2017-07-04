---
layout: default
title: instance method PlatoDevice::XBeeWiFi#available
---

## available -> Fixnum

XBee WiFi通信モジュールに受信しているデータ長を返します。  

|引数|
|:--|
|なし|

|戻り値||
|:--|:--|
|Fixnum|XBee WiFi通信モジュールに受信しているデータ長が返されます。受信データがない場合は0が返されます。|

### 例:
```Ruby
wifi = PlatoDevice::XBeeWiFi.open       # XBee通信モジュールをオープンします
wifi.connect('192.168.1.1', 20000)      # 192.168.1.1:20000 に接続します
loop {
  while wifi.available == 0             # XBeeからデータを受信するまで
    Plato::Machine.delay(10)            # 10ミリ秒待ちます
  end
  print sprintf("%02X ", wifi._read)    # 受信データを16進表示します
}
```
