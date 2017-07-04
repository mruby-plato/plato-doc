# singleton method Plato::Machine.millis

## millis -> Fixnum

マイコンボードが起動してから経過した時間をミリ秒で返します。  

|引数|
|:--|
|なし|

|戻り値||
|:--|:--|
|Fixnum|起動してからの経過時間(ミリ秒)|

### 例:
```Ruby
io = Plato::DigitalIO.new(0)
t = Plato::Machine.millis     # 現在の経過時間を取得
10.times {
  p io.read
  Plato::Machine.delay(500)
}
p Plato::Machine.millis - t   # 経過時間を表示
```
