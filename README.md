# Mvc5FisrtSample
リレーションのあるテーブルが3つの、シンプルな MVC5 サンプルアプリです。

## サンプルアプリ概要
### MVC 関係
- スキャフォールディングで各テーブルのコントローラー、ビューをぱっと作って済ませる。
- 認証なし

### データベース関係
- データベース名: ApplicationDb
- テーブル
  - Parents
  - Children
  - Sexes ← 男、女が入っているだけのマスタテーブル
- リレーション
  - Parents 1-n Children
  - Parents n-1 Sexes
  - Children n-1 Sexes
- レコードから見るテーブルのリレーション表現は
  - Parents には Children 関係のカラムは無い。
  - Children は ParentsId カラムを持ち、親を指定する。
  - Parents と Children は SexId を持ち、性別を指定する。
  - Sexes には、他テーブル関係のカラムは無い。
