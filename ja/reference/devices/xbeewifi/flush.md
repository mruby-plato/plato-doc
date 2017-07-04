---
layout: default
title: instance method PlatoDevice::XBeeWiFi#flush
---

## flush -> nil

XBee WiFi通信モジュールの送信バッファをフラッシュします。  

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
"Hello, Plato!\n".each_byte do |dt|
  wifi._write(dt)   # XBeeに1バイトずつデータを出力します
end
wifi.flush          # フラッシュして送信完了を待ちます
```
