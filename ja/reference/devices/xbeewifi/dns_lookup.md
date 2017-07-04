---
layout: default
title: instance method PlatoDevice::XBeeWiFi#dns_lookup
---

## dns_lookup(fqdn) -> String

WiFiネットワーク上のDNSサーバにホスト名の問い合わせを行います。  
名前解決に失敗した場合は RuntimeError となります。

|引数||
|:--|:--|
|fqdn|DNSサーバに問い合わせるホスト名を指定します。|

|戻り値||
|:--||
|String|DNS問い合わせ結果のIPアドレスが返されます。|

### 例:
```Ruby
wifi = PlatoDevice::XBeeWiFi.open       # XBee WiFi通信モジュールをオープンします
begin
  puts wifi.dns_lookup('hogehoge.com')  # => 'xxx.xxx.xxx.xxx'
rescue => e
  p e
end
```
