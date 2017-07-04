# module Plato::Serial

### モジュールの継承リスト: Plato::Serial

## 要約

UARTなどのシリアルI/Fへの入出力操作を定義したモジュールです。  

## 特異メソッド

|定義|説明|
|:--|:--|
|[register_device(device) -> Object](register_device.md)|シリアルI/Fデバイスを登録します。|
|[open(baud, dbits=8, start=1, stop=1, parity=:none) -> Object](open.md)|シリアルI/Fデバイスをオープンし、シリアルI/Fデバイスクラスのインスタンスを返します。|

## インスタンスメソッド

|定義|説明|
|:--|:--|
|[_read -> Fixnum](raw_read.md)|シリアルI/Fデバイスから1バイトのデータを読み込みます。|
|[_write(data) -> nil](raw_write.md)|シリアルI/Fデバイスに1バイトのデータを書き込みます。|
|[available -> Fixnum](available.md)|シリアルI/Fデバイスに受信しているデータ長を返します。|
|[flush -> nil](flush.md)|シリアルI/Fの送信バッファをフラッシュします。|
|[close -> nil](close.md)|シリアルI/Fデバイスをクローズします。|
|[read(len=nil, type=:as_array, tmo=2000) -> Array \| String](read.md)|シリアルI/Fデバイスから読み込んだデータを返します。|
|[write(data) -> nil](write.md)|シリアルI/Fデバイスにデータを出力します。|
|[getc -> String \| nil](getc.md)|シリアルI/Fデバイスから1バイトのデータを読み込み、文字データとして返します。|
|[putc(data) -> nil](putc.md)|シリアルI/Fデバイスに1文字のデータを出力します。|
|[gets(rs="\n") -> String \| nil<br>gets(limit) -> String \| nil<br>gets(rs, limit) -> String \| nil](gets.md)|シリアルI/Fデバイスから1行分のデータ読み込み、文字列として返します。|
|[puts(*data) -> nil](puts.md)|シリアルI/Fデバイスに指定されたデータに改行を付加した文字列を出力します。|
|[print(*data) -> nil](print.md)|シリアルI/Fデバイスに指定されたデータを文字列として出力します。|
|[self << data -> self](lshift.md)|シリアルI/Fデバイスに指定されたデータを文字列として出力します。|
|[term_char = cr -> nil](term_char.md)|入出力の区切り文字(行の終端文字)を指定します。|
