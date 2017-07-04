# class Plato::RTC

### クラスの継承リスト: Plato::RTC < Object

## 要約

RTC(Real Time Clock)の制御を行うための抽象クラスです。  
RTCに対して時刻取得および時刻設定を行う機能を提供します。  
実際のRTCデバイスに対する制御はRTCデバイスの仕様によって異なるため、RTCデバイス毎に定義されるRTCのサブクラスで行われます。

## 特異メソッド

|定義|説明|
|:--|:--|
|[set_time(time) -> nil](set_time.md)|RTCの時刻を設定します。|
|[get_time -> Object](get_time.md)|RTCから現在時刻を取得します。|
