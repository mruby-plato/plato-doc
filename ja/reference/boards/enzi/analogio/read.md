# instance method Plato::AnalogIO#read

## read -> Fixnum

enziボードのアナログIOから入力したアナログ値を返します。  
enziボードではA0〜A5のPINがアナログ入力が可能なPINです。  
アナログ入力を行う場合には[Plato::AnalogIO.new](../../../plato/analogio/new.md)でPIN番号に上記のいずれかを指定して下さい。

|引数|
|:--|
|なし|

|戻り値||
|:--|:--|
|Fixnum|アナログIOから入力した値(0〜1023)|

### 例:
```Ruby
io = Plato::AnalogIO.new(A0)
p io.read           # -> 0 〜 1023
```
