---
layout: default
title: instance method PlatoDevice::XBeeWiFi#_read
---

## _read -> Fixnum

XBee WiFi通信モジュールから1バイトのデータを読み込みます。  

|引数|
|:--|
|なし|

|戻り値||
|:--|:--|
|Fixnum|XBee WiFiから読み込んだデータ(0〜255)が返されます。受信データがない場合は-1が返されます。|

### 例:
```Ruby
wifi = PlatoDevice::XBeeWiFi.open   # XBee WiFi通信モジュールをオープンします
wifi.connect('192.168.1.1', 20000)  # 192.168.1.1:20000 に接続します
loop {
  dt = wifi._read                   # XBee WiFiから1バイト読み込みます
  if dt >= 0                        # データを受信した場合は
    print sprintf("%02X ", dt)      # 受信データを16進表示します
  end
}
```
