# instance method Plato::LED#toggle

## toggle -> nil

LEDの点灯状態を点灯(ON)から消灯(OFF)、または消灯(OFF)から点灯(ON)に切り替えます。

|引数|
|:--|
|なし|

|戻り値|
|:--|
|nil|

### 例:
```Ruby
led = Plato::LED.new(0)
led.off
50.times {
  led.toggle    # LEDの点灯状態を切り替えます
  Plato::Machine.delay(100)
}
```
