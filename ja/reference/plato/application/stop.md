# instance method Plato::MRubyApplication#stop

## stop -> nil

アプリケーションを停止します。  

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
    if @tm <= Plato::Machine.millis   # 開始から10秒(10000ミリ秒)を経過したら
      stop                            # アプリケーションを停止します
    end
  end
end
MyApplication.new.start
```
