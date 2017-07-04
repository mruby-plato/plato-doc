# instance method Plato::DigitalIO#write

## write(data) -> Fixnum

enziボードのディジタルIOに指定した値を出力します。  

|引数||
|:--|:--|
|data|出力する値(0または1)を指定します。|

|戻り値||
|:--|:--|
|Fixnum|出力した値(0または1)が返されます。|

### 例:
```Ruby
io = Plato::DigitalIO.new(D0)
io.write(0)             # 0番PINに0を出力します
io.write(Plato::HIGH)   # 0番PINにHIGH(1)を出力します
```
