# class Plato::ZigBee

### クラスの継承リスト: Plato::ZigBee < [Plato::Serial](../serial/README.md) < Object

## 要約

ZigBee通信デバイスの制御を行うための抽象クラスです。  
実際のZigBee通信デバイスに対する制御はデバイスの仕様によって異なるため、ZigBeeデバイス毎に定義されるZigBeeのサブクラスで行われます。

## 特異メソッド

|定義|説明|
|:--|:--|
|[open(panid) -> Object](open.md)|ZigBeeデバイスをオープンし、ZigBeeデバイスクラスのインスタンスを返します。|

## インスタンスメソッド

|定義|説明|
|:--|:--|
|[connect(adrh, adrl) -> nil](connect.md)|ZigBeeネットワークに接続します。|
