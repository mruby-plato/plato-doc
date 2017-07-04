# class PlatoDevice::XBee

### クラスの継承リスト: PlatoDevice::XBee < [Plato::ZigBee](../../plato/zigbee/README.md) < [Plato::Serial](../../plato/serial/README.md) < Object

## 要約

XBee ZigBee通信モジュールのデバイスクラスです。

## 特異メソッド

|定義|説明|
|:--|:--|
|[open(pan=nil) -> Plato::XBee](open.md)|XBee通信モジュールをオープンして、XBeeクラスのインスタンスを返します。|

## インスタンスメソッド

|定義|説明|
|:--|:--|
|[_read -> Fixnum](raw_read.md)|XBee通信モジュールから1バイトのデータを読み込みます。|
|[_write(data) -> nil](raw_write.md)|XBee通信モジュールに1バイトのデータを書き込みます。|
|[available -> Fixnum](available.md)|XBee通信モジュールに受信しているデータ長を返します。|
|[flush -> nil](flush.md)|XBee通信モジュールの送信バッファをフラッシュします。|
|[close -> nil](close.md)|XBee通信モジュールをクローズします。|
|[panid = id -> nil](set_panid.md)|XBee通信モジュールのPAN IDを設定します。|
|[panid -> String](get_panid.md)|XBee通信モジュールに設定されているPAN IDを取得します。|
|[connections -> Array](connections.md)|ペアリングされたZigBeeデバイスのアドレスを取得します。|
|[my_address -> Array](my_address.md)|XBee通信モジュールのアドレスを取得します。|
|[reset -> nil](reset.md)|XBee通信モジュールのネットワーク設定をリセットします。|
|[save -> nil](save.md)|XBee通信モジュールの設定を保存します。|
