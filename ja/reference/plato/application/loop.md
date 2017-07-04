# instance method Plato::MRubyApplication#_loop

## _loop -> nil

[MRubyApplication#start](start.md)の実行によってアプリケーションが実行されると、アプリケーションのバックグラウンド処理として呼び出されます。  
アプリケーションが実行されるとこの処理は1ミリ秒以上の間隔で連続で呼び出されます。[MRubyApplication#add_timer](add_timer.md)で登録されたタイマ処理の呼び出しタイミングとなった場合は、タイマ処理の実行が優先されます。  
タイマ処理起動のための時間監視はMRubyApplicationクラスの内部処理で行われるため、[_loop](_loop.md)処理内では[Plato::Machine.delay](../machine/delay.md)などの時間遅延が発生する処理を呼び出さないで下さい。

|引数|
|:--|
|なし|

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
    add_timer(500, Proc.new {|app| app.blink})  # MyApplication#blinkを呼び出す処理を500ミリ秒周期で実行
  end

  def blink
    @led.toggle
  end

  def _loop
    if @tm <= Plato::Machine.millis   # 開始から10秒(10000ミリ秒)を経過したら
      stop                            # アプリケーションを停止します
    end
  end
end
MyApplication.new.start   # アプリケーション実行
```
