# instance method Plato::MRubyApplication#start

## start -> nil

アプリケーションを実行します。  
[MRubyApplication#add_timer](add_timer.md)で登録したタイマ処理の周期呼び出し、[MRubyApplication#_loop](_loop.md)のバックグラウンド呼び出しが繰り返されます。  
アプリケーションを停止するためには[MRubyApplication#stop](stop.md)を呼び出します。

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
    add_timer(500, Proc.new {|app| app.blink})  # MyApplication#blinkを呼び出す処理を500ミリ秒周期で実行
  end

  def blink
    @led.toggle
  end
end
MyApplication.new.start   # アプリケーション実行
```
