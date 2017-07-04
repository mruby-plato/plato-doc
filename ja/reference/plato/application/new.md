# singleton method Plato::MRubyApplication.new

## new -> MRubyApplication

mrubyアプリケーションのオブジェクトを生成して返します。  
Rubyでは**new**メソッドが呼び出されると、オブジェクト生成後に**initialize**メソッドが呼び出されます。
MRubyApplicationクラスのサブクラスとしてユーザ独自のアプリケーションクラスを作成した場合には、**initialize**メソッドの中でアプリケーションの初期化処理を記述することができます。

|引数|
|:--|
|なし|

|戻り値||
|:--|:--|
|MRubyApplication|生成したMRubyApplicationオブジェクト|

### 例:
```Ruby
class MyApplication < MRubyApplication  # MRubyApplicationのサブクラスを定義
  def initialize
    super   # MRubyApplicationのinitaializeを呼び出します
    # アプリケーション独自の初期化処理
    @led = Plato::LED.new(0)
    add_timer(500, Proc.new {|app| app.blink})
  end

  def blink
    @led.toggle
  end
end

app = MyApplication.new     # アプリケーションオブジェクトを生成 (initializeが呼び出されます)
app.start
```
