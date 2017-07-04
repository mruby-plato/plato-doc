# class PlatoDevice::XBeeWiFi

### クラスの継承リスト: PlatoDevice::XBeeWiFi < [Plato::WiFi](../../plato/wifi/README.md) < [Plato::Serial](../../plato/serial/README.md) < Object

## 要約

XBee WiFi通信モジュールのデバイスクラスです。

## 特異メソッド

|定義|説明|
|:--|:--|
|[open -> Plato::XBeeWiFi](open.md)|XBee WiFi通信モジュールをオープンして、WiFiクラスのインスタンスを返します。|

## インスタンスメソッド

|定義|説明|
|:--|:--|
|[_read -> Fixnum](raw_read.md)|XBee WiFi通信モジュールから1バイトのデータを読み込みます。|
|[_write(data) -> nil](raw_write.md)|XBee WiFi通信モジュールに1バイトのデータを書き込みます。|
|[available -> Fixnum](available.md)|XBee WiFi通信モジュールに受信しているデータ長を返します。|
|[flush -> nil](flush.md)|XBee WiFi通信モジュールの送信バッファをフラッシュします。|
|[close -> nil](close.md)|XBee WiFi通信モジュールをクローズします。|
|[connect(dest, port=80) -> nil](connect.md)|WiFiネットワーク上の指定アドレス／ポートに接続します。|
|[ping(ip) -> String](ping.md)|指定IPアドレスに対してPINGを発行します。|
|[mac_address -> String](mac_address.md)|XBee WiFi通信モジュールのMACアドレスを取得します。|
|[dns_lookup(fqdn) -> String](dns_lookup.md)|WiFiネットワーク上のDNSサーバにホスト名の問い合わせを行います。|
|[scan_ap -> Array](scan_ap.md)|XBee WiFiが接続可能なアクセスポイントの一覧を取得します。|
