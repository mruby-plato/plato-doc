# instance method Plato::DigitalIO#read

## read -> Fixnum

enziボードのディジタルIOから入力したディジタル値を返します。  

|引数|
|:--|
|なし|

|戻り値||
|:--|:--|
|Fixnum|ディジタルIOから入力した値(0または1)|

### 例:
```Ruby
io = Plato::DigitalIO.new(D0)
p io.read           # -> 0 | 1
```
