# class Plato::MRubyApplication

### クラスの継承リスト: Plato::MRubyApplication < Object

## 要約

典型的なmruby組込みアプリケーションに必要なタイマ処理等の機能を提供するクラスです。  
このクラスを継承したサブクラスを作成することで、ユーザ独自のmrubyアプリケーションを作成することができます。

## 特異メソッド

|定義|説明|
|:--|:--|
|[new -> MRubyApplication](new.md)|mrubyアプリケーションのオブジェクトを生成して返します。|

## インスタンスメソッド

|定義|説明|
|:--|:--|
|[add_timer(ms, proc) -> Fixnum](add_timer.md)|タイマ処理を登録します。|
|[delete_timer(id) -> nil](delete_timer.md)|タイマ処理を削除します。|
|[start -> nil](start.md)|アプリケーションを開始します。|
|[stop -> nil](stop.md)|アプリケーションを停止します。|
|[_loop -> nil](loop.md)|アプリケーションのバックグラウンド処理として呼び出されるメソッドです。|
|[running? -> true \| false](isrunning.md)|アプリケーションが開始されたかどうかの判定結果を返します。|
