# singleton method Plato::Timer.delete

## delete(id) -> nil

指定したタイマIDのタイマ処理を停止・削除します。  

|引数||
|:--|:--|
|id|削除対象のタイマ処理のIDを指定します。(タイマIDは[add](add.md)の戻り値として返されます)|

|戻り値|
|:--|
|nil|

### 例:
```Ruby
prc = Proc.new {|arg| puts arg}
lmd = lambda {|arg| puts arg * 2}
tid1 = Plato::Timer.add(1000, prc, "Proc")   # Procを1秒周期起動で登録します
tid2 = Plato::Timer.add(2000, lmd, "lambda") # lambdaを2秒周期起動で登録します
et = Plato::Machine.millis + 10000
Plato::Timer.start
loop {
  if et < Plato::Machine.millis   # 10秒経過したら
    Plato::Timer.delete(tid1)     # Procの周期起動を停止します
  end
  Plato::Timer.refresh
  Plato::Machine.delay(1)
}
```
