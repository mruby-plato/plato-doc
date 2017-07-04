# instance method Plato::MRubyApplication#add_timer

## add_timer(ms, proc) -> Fixnum

指定した周期で起動されるタイマ処理を登録します。  

|引数||
|:--|:--|
|ms|タイマ処理の起動周期をミリ秒単位で指定します。|
|proc|周期呼び出しするタイマ処理(Proc または lambda)を指定します。呼び出されるタイマ処理には引数1つ(アプリケーションオブジェクト)が渡されます。|

|戻り値||
|:--|:--|
|Fixnum|タイマID (delete_timerでタイマ処理を削除する際に使用します)|

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
MyApplication.new.start
```
