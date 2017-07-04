# singleton method PlatoEnzi::Machine.delay_us

## delay_us(us) -> nil

指定した時間(マイクロ秒)だけ処理を停止します。  
[Plato::Machine.delay_us](../../../plato/machine/delay_us.md)から呼び出されます。

|引数||
|:--|:--|
|us|停止する時間をマイクロ秒単位で指定します。|

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
  Plato::Machine.delay_us(10000)  # 10000マイクロ秒停止します
}
```
