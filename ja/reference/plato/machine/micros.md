# singleton method Plato::Machine.micros

## micros -> Fixnum

マイコンボードが起動してから経過した時間をマイクロ秒で返します。  

|引数|
|:--|
|なし|

|戻り値||
|:--|:--|
|Fixnum|起動してからの経過時間(マイクロ秒)|

### 例:
```Ruby
io = Plato::DigitalIO.new(0)
t = Plato::Machine.micros     # 現在の経過時間を取得
10.times {
  p io.read
  Plato::Machine.delay_us(500)
}
p Plato::Machine.micros - t   # 経過時間を表示
```
