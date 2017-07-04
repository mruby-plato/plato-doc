# singleton method Plato::Timer.start

## start(id=nil) -> nil

[add_timer](add_timer.md)で登録したタイマ処理の起動周期監視を初期化し、タイマ処理起動監視を開始します。  
タイマ処理を周期的に実行するためには[refresh](refresh_s.md)を繰り返し呼び出す必要があります。

|引数||
|:--|:--|
|id=nil|開始処理を行うタイマ処理をタイマIDで指定します。<br>タイマIDに**nil**(デフォルト)を指定した場合は、登録されている全てのタイマ処理の開始処理が行われます。|

|戻り値|
|:--|
|nil|

### 例:
```Ruby
prc = Proc.new {|arg| puts arg}
lmd = lambda {|arg| puts arg * 2}
tid1 = Plato::Timer.add_timer(1000, prc, "Proc")   # Procを1秒周期起動で登録します
tid2 = Plato::Timer.add_timer(2000, lmd, "lambda") # lambdaを2秒周期起動で登録します
Plato::Timer.start
5555.times {
  Plato::Timer.refresh
  Plato::Machine.delay(1)
}
Plato::Timer.start(tid2)    # tid2のタイマ処理(lambda)のタイマ監視を初期化します
loop {
  Plato::Timer.refresh
  Plato::Machine.delay(1)
}
```
