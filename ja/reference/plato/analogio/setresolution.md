# instance method Plato::AnalogIO#resolution=

## resolution=reso -> Fixnum

アナログ入力の分解能をビット数で指定します。
使用するマイコンボードによって仕様が異なるため、マイコンボード毎にライブラリが用意されています。

|引数||
|:--|:--|
|reso|アナログ入力の分解能(ビット数)を指定します。|

|戻り値||
|:--|:--|
|Fixnum|設定した分解能の値が返されます。|

### 例:
```Ruby
io = Plato::AnalogIO.new(0)
io.resolution = 8       # アナログ入力の分解能を8bitに設定します。
```
