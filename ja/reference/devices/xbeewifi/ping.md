---
layout: default
title: instance method PlatoDevice::XBeeWiFi#ping
---

## ping(ip) -> String

指定IPアドレスに対してPINGを発行します。  

|引数||
|:--|:--|
|ip|接続確認するIPアドレスを'xxx.xxx.xxx.xxx'の形式の文字列で指定します。|

|戻り値||
|:--||
|String|応答が帰ってきた場合には'OK'が返されます。|

### 例:
```Ruby
wifi = PlatoDevice::XBeeWiFi.open       # XBee WiFi通信モジュールをオープンします
begin
  wifi.connect('192.168.1.1', 20000)    # 192.168.1.1:20000 に接続します
  wifi.puts 'Hello'
rescue => e
  p e
end
```
