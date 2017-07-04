# singleton method Plato::Timer.refresh

## refresh -> nil

[add_timer](add_timer.md)で登録したタイマ処理の起動周期監視を行い、指定された起動タイミングにタイマ処理を実行します。  
タイマ処理を周期的に実行するためには、このメソッドを繰り返し呼び出す必要があります。

|引数|
|:--|
|なし|

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
loop {
  Plato::Timer.refresh        # タイマ処理（tid1, tid2) が周期的に実行されます
  Plato::Machine.delay(1)
}
```
