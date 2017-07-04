# instance method Plato::MRubyApplication#delete_timer

## delete_timer(id) -> nil

指定したタイマIDのタイマ処理を停止・削除します。  

|引数||
|:--|:--|
|id|削除対象のタイマ処理のIDを指定します。(タイマIDはadd_timerの戻り値として返されます)|

|戻り値|
|:--|
|nil|

### 例:
```Ruby
class MyApplication < MRubyApplication
  def initialize
    super
    @led = Plato::LED.new(0)
    @tm = Plato::Machine.millis + 10000
    @tid = add_timer(500, Proc.new {|app| app.blink})
  end

  def blink
    @led.toggle
    if @tm <= Plato::Machine.millis   # 開始から10秒(10000ミリ秒)を経過したら
      delete_timer(@tid)              # タイマ処理削除
    end
  end
end
MyApplication.new.start
```
