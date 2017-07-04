# class Plato::Timer

### クラスの継承リスト: Plato::Timer < [Plato::Machine](../machine/README.md) < Object

## 要約

タイマ起動機能を提供するクラスです。  
Plato::Timerクラスが提供するタイマ起動機能は、ソフトウェアの起動タイミング監視によって実現されているため、リアルタイム性が保証されないことに注意して下さい。

## 特異メソッド

|定義|説明|
|:--|:--|
|[add(ms, proc, arg=nil) -> Fixnum](add.md)|タイマ処理を登録します。|
|[delete(id) -> nil](delete.md)|タイマ処理を停止・削除します。|
|[start(id=nil) -> nil](start.md)|タイマ処理起動監視を開始します。|
|[stop(id=nil) -> nil](stop.md)|タイマ処理起動監視を停止します。|
|[refresh -> nil](refresh.md)|タイマ処理起動監視を実施します。|
