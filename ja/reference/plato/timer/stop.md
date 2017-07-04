# singleton method Plato::Timer.stop

## stop(id=nil) -> nil

[add_timer](add_timer.md)で登録したタイマ処理の起動周期監視を停止し、タイマ処理を削除します。  

|引数||
|:--|:--|
|id=nil|停止・削除するタイマ処理をタイマIDで指定します。<br>タイマIDに**nil**(デフォルト)を指定した場合は、登録されている全てのタイマ処理の停止・削除処理が行われます。|

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
Plato::Timer.stop(tid2)   # tid2のタイマ処理(lambda)のタイマ処理を停止・削除します
4444.time {
  Plato::Timer.refresh
  Plato::Machine.delay(1)
}
Plato::Timer.stop         # 全てのタイマ処理を停止・削除します
```
