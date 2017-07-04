---
layout: default
title: instance method Plato::AnalogIO#write
---

## write(data) -> Fixnum

enziボードのアナログIOに指定した値を出力します。  
enziボードではD3,D5,D6,D8,D9,D10のPINがアナログ出力(PWM出力)が可能なPINです。  
アナログ出力を行うには[Plato::AnalogIO.new](../../analogio/new.html)でPIN番号に上記のいずれかを指定して下さい。

|引数||
|:--|:--|
|data|出力する値(0〜255)を指定します。|

|戻り値||
|:--|:--|
|Fixnum|出力した値(0〜255)が返されます。|

### 例:
```Ruby
io = Plato::DigitalIO.new(D8)
io.write(255)           # D8 PINに255を出力します
```
