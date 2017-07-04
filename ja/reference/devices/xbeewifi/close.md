---
layout: default
title: instance method PlatoDevice::XBeeWiFi#close
---

## close -> nil

XBee WiFi通信モジュールをクローズします。  

|引数|
|:--|
|なし|

|戻り値|
|:--|
|なし|

### 例:
```Ruby
wifi = PlatoDevice::XBeeWiFi.open   # XBee WiFi通信モジュールをオープンします
wifi.connect('192.168.1.1', 20000)  # 192.168.1.1:20000 に接続します
[79, 75, 10].each do |dt|
  wifi._write(dt)   # XBee通信モジュールに 79, 75, 10 の順に出力します
end
wifi.close          # XBee通信モジュールをクローズします
```
