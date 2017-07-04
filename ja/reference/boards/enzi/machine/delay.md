# singleton method PlatoEnzi::Machine.delay

## delay(ms) -> nil

指定した時間(ミリ秒)だけ処理を停止します。  
[Plato::Machine.delay](../../../plato/machine/delay.md)から呼び出されます。

|引数||
|:--|:--|
|ms|停止する時間をミリ秒単位で指定します。|

|戻り値|
|:--|
|nil|

### 例:
```Ruby
io = Plato::DigitalIO.new(0)
a = 1
10.times {
  io.write(a)
  a ^= 1
  Plato::Machine.delay(100)     # 100ミリ秒停止します
}
```
