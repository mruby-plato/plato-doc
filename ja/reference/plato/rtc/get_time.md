# instance method Plato::RTC#get_time

## get_time -> Object

RTCから現在時刻を取得します。  
取得できる日時の形式は、RTCデバイス毎に提供されるRTCのサブクラスの実装に依存します。

|引数|
|:--|
|なし|

|戻り値||
|:--|:--|
|Object|現在時刻の情報が返されます。戻り値の内容はサブクラスに実装されたget_timeメソッドに依存します。|

### 例:
このメソッドではRTCデバイスへの操作は行われないため、直接使用しても効果がありません。  
