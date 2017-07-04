# instance method Plato::MRubyApplication#running?

## running? -> nil

アプリケーションが開始されたかどうかの判定結果を返します。  

|引数|
|:--|
|なし|

|戻り値||
|:--|:--|
|true \| false|アプリケーションが実行中の場合は**true**、実行中でない場合は**false**を返します。|

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
    p running?    # -> true
  end
end
app = MyApplication.new
p app.running?    # -> false
app.start         # アプリケーション実行
```
