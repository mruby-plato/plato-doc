# module Plato::Machine

### モジュールの継承リスト: Plato::Machine

## 要約

マシン(マイコンボード)に依存する各種制御を定義したモジュールです。

## 特異メソッド

|定義|説明|
|:--|:--|
|[delay(ms) -> nil](delay.md)|指定した時間(ミリ秒)だけ処理を停止します。|
|[delay_us(us) -> nil](delay_us.md)|指定した時間(マイクロ秒)だけ処理を停止します。|
|[micros -> Fixnum](micros.md)|マイコンボードが起動してから経過した時間をマイクロ秒で返します。|
|[millis -> Fixnum](millis.md)|マイコンボードが起動してから経過した時間をミリ秒で返します。|
|[register_device(device) -> Object](register_device.md)|マシン(マイコンボード)デバイスを登録します。|
