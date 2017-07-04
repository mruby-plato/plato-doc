---
layout: default
title: instance method PlatoDevice::XBeeWiFi#connect
---

## connect(dest, port=80) -> nil

WiFiネットワーク上の指定アドレス／ポートに接続します。  
接続に失敗した場合は、RuntimeErrorが発生します。

|引数||
|:--|:--|
|dest|接続先のIPアドレス('xxx.xxx.xxx.xxx'形式の文字列)を指定します。|
|port|接続先のポート番号を指定します。省略した場合は80番ポートに接続します。|

|戻り値|
|:--|
|なし|

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
