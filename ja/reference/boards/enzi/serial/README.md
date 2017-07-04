# class PlatoEnzi::Serial

### クラスの継承リスト: PlatoEnzi::Serial < [Plato::Serial](../../../plato/serial/README.md) < Object

## 要約

enziボードのシリアルI/F(UART)への入出力機能を提供するクラスです。  
D0 PINがRX(enziへの入力)、D1 PINがTX(enziからの出力)に割り当てられます。

## 特異メソッド

|定義|説明|
|:--|:--|
|[new(baud, dbits=8, start=1, stop=1, parity=:none) -> PlatoEnzi::Serial](new.md)|シリアルI/F(UART)デバイスをオープンし、シリアルI/Fデバイスのオブジェクトを返します。|

## インスタンスメソッド

|定義|説明|
|:--|:--|
|[_read -> Fixnum](raw_read.md)|シリアルI/Fから1バイトのデータを読み込みます。|
|[_write(data) -> nil](raw_write.md)|シリアルI/Fに1バイトのデータを書き込みます。|
|[available -> Fixnum](available.md)|シリアルI/Fに受信しているデータ長を返します。|
|[flush -> nil](flush.md)|シリアルI/Fの送信バッファをフラッシュします。|
|[close -> nil](close.md)|シリアルI/Fデバイスをクローズします。|
