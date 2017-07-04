# singleton method Plato::ZigBee.open

## open(panid) -> Object

ZigBeeデバイスをオープンし、ZigBeeデバイスクラスのインスタンスを返します。  
ZigBeeデバイスの初期化処理はデバイス毎に異なるため、実際のオープン処理はZigBeeデバイス毎のサブクラスにて実施されます。

|引数||
|:--|:--|
|panid|PAN ID(ZigBeeネットワークの識別子)を指定します。|

|戻り値||
|:--|:--|
|Object|ZigBeeデバイスクラスのインスタンス|

### 例:
このメソッドではZigBeeデバイスへの操作は行われないため、使用しても効果がありません。  
