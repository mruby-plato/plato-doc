# instance method PlatoDevice::XBeeWiFi#dns_lookup

## scan_ap -> Array

XBee WiFiが接続可能なアクセスポイントの一覧を取得します。  

|引数|
|:--|
|なし|

|戻り値||
|:--||
|Array|検出されたアクセスポイントの情報が配列で返されます。アクセスポイントの情報はSSIDとセキュリティタイプ(:none, :wep, :wpa1, :wpa2)の配列になります。|

### 例:
```Ruby
wifi = PlatoDevice::XBeeWiFi.open       # XBee WiFi通信モジュールをオープンします
puts wifi.scan_ap                       # => ['AP001', :wpa2]
                                        #    ['PublicAP', :none]
                                        #    ['AP002', :wpa1]
```
