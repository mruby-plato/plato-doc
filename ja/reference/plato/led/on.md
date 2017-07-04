# instance method Plato::LED#on

## on -> nil

LEDをON(点灯)します。

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
