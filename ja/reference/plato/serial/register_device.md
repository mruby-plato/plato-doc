# singleton method Plato::Serial.register_device

## register_device(device) -> Object

シリアルI/Fデバイスクラスを登録します。  
PlatoIDEで生成したアプリケーションでは使用するマイコンボード用のマシンデバイスクラスが自動登録されるため、本メソッドを使用する必要はありません。

|引数||
|:--|:--|
|device|マイコンボードに依存するシリアルI/Fデバイスクラスを指定します。<br>指定するシリアルI/Fデバイスクラスは以下のメソッドが実装されている必要があります。<br>- [open](open.md)<br>- [_read](raw_read.md)<br>- [_write](raw_write.md)<br>- [available](availablle.md)<br>- [flush](flush.md)<br>- [close](close.md)|

|戻り値||
|:--|:--|
|Object|登録したシリアルI/Fデバイスクラス|

### 例:
```Ruby
Plato::Serial.register_device(PlatoEnzi::Serial)    # enziボードのシリアルI/Fデバイスクラスを登録します
ser = Plato::Serial.open(9600)  # enziボードに接続されたシリアルI/Fデバイスをオープンします
```
