# instance method Plato::GPIO#read

## read -> Object

GPIO(汎用IO)から値を入力するための雛形のメソッドです。  
実際のIOからの入力はGPIOクラスを継承したサブクラス側で行います。

|引数|
|:--|
|なし|

|戻り値||
|:--|:--|
|Object|戻り値の内容はサブクラスに実装されたreadメソッドに依存します。|

### 例:
このメソッドではIOへの操作は行われないため、使用しても効果がありません。  