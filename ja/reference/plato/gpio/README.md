# class Plato::GPIO

### クラスの継承リスト: Plato::GPIO < Object

## 要約

GPIO(汎用IO)デバイスの制御を行うためのクラスです。  
ディジタルIO、アナログIOに対する汎用的な機能を提供します。

## 定数

|定義|説明|
|:--|:--|
|LOW|LOWレベル(0)|
|HIGH|HIGHレベル(1)|

## 特異メソッド

|定義|説明|
|:--|:--|
|[new(pin) -> GPIO](new.md)|指定したPINに割り付けられたGPIO(汎用IO)デバイスのオブジェクトを生成して返します。|

## インスタンスメソッド

|定義|説明|
|:--|:--|
|[high -> Fixnum](high.md)|GPIOにHIGHを出力します。|
|[high? -> true \| false](ishigh.md)|GPIOがHIGHレベルかどうかを判定した結果を返します。|
|[low -> Fixnum](low.md)|GPIOにLOWを出力します。|
|[low? -> true \| false](islow.md)|GPIOがLOWレベルかどうかを判定した結果を返します。|
|[read -> Object](read.md)|GPIOから値を入力するための雛形のメソッドです。|
|[write(data) -> Object](write.md)|GPIOに指定した値を出力するための雛形のメソッドです。|
