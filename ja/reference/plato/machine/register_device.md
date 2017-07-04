# singleton method Plato::Machine.register_device

## register_device(device) -> Object

マシン(マイコンボード)デバイスクラスを登録します。  
PlatoIDEで生成したアプリケーションでは使用するマイコンボード用のマシンデバイスクラスが自動登録されるため、本メソッドを使用する必要はありません。

|引数||
|:--|:--|
|device|マシン(マイコンボード)に依存する各種操作を行うマシンデバイスクラスを指定します。|

|戻り値||
|:--|:--|
|Object|登録したマシンデバイスクラス|

### 例:
```Ruby
Plato::Machine.register_device(PlatoEnzi::Machine)  # enziボードのマシンデバイスを登録します
Plato::Machine.delay(1000)    # enziボード用のdelay処理が呼び出されます
```
