# instance method Plato::LED#off

## off -> nil

LEDをOFF(消灯)します。

|引数|
|:--|
|なし|

|戻り値|
|:--|
|nil|

### 例:
```Ruby
led = Plato::LED.new(0)
led.on      # 0番PINに接続されたLEDを点灯します
led.off     #                 LEDを消灯します
```
