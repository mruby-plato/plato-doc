---
layout: default
title: instance method PlatoDevice::XBeeWiFi#mac_address
---

## mac_address -> String

XBee WiFi通信モジュールのMACアドレスを取得します。  

|引数|
|:--|
|なし|

|戻り値||
|:--||
|String|XBee WiFi通信モジュールのMACアドレスが12桁の16進数文字列で返されます。|

### 例:
```Ruby
wifi = PlatoDevice::XBeeWiFi.open       # XBee WiFi通信モジュールをオープンします
puts wifi.mac_address   # => '0001AB4A6E20'
```
