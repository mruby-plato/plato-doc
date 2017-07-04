---
layout: default
title: instance method PlatoDevice::XBeeWiFi#_write
---

## _write(data) -> nil

XBee WiFi通信モジュールに1バイトのデータを書き込みます。  

|引数||
|:--|:--|
|data|XBee WiFi通信モジュールに書き込むバイトデータ(0〜255の数値)を指定します。|

|戻り値|
|:--|
|なし|

### 例:
```Ruby
wifi = PlatoDevice::XBeeWiFi.open   # XBee WiFi通信モジュールをオープンします
wifi.connect('192.168.1.1', 20000)  # 192.168.1.1:20000 に接続します
[79, 75, 10].each do |dt|
  wifi._write(dt)                   # XBee WiFi通信モジュールに 79, 75, 10 の順に出力します
end
```
