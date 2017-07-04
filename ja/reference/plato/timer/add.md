# singleton method Plato::Timer.add

## add(ms, proc, arg=nil) -> Fixnum

タイマ処理を登録します。  

|引数||
|:--|:--|
|ms|タイマ処理の起動周期をミリ秒単位で指定します。|
|proc|周期呼び出しするタイマ処理(Proc または lambda)を指定します。呼び出されるタイマ処理には**arg**が引数として渡されます。|
|arg=nil|タイマ処理に渡される引数を指定します。|

|戻り値||
|:--|:--|
|Fixnum|タイマID ([delete](delete.md)でタイマ処理を削除する際に使用します)|

### 例:
```Ruby
prc = Proc.new {|arg| puts arg}
lmd = lambda {|arg| puts arg * 2}
tid1 = Plato::Timer.add(1000, prc, "Proc")   # Procを1秒周期起動で登録します
tid2 = Plato::Timer.add(2000, lmd, "lambda") # lambdaを2秒周期起動で登録します
Plato::Timer.start
loop {
  Plato::Timer.refresh
  Plato::Machine.delay(1)
}
```
