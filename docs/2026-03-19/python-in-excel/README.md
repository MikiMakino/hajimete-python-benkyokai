# 2026-03-19 Python in Excel 勉強会

## テーマ：売上データを使って、表をまとめて扱う体験をする

Excel を使いながら **Python in Excel** の基本を体験します。
特に「表全体をまとめて扱う」感覚を身につけることを目指します。

---

## この日に学ぶこと

- `=PY()` を使って Python を動かす
- Excel の表を Python で扱う
- 基本集計をする（合計・平均・最大値・最小値・件数）
- 条件でデータを絞り込む

---

## 準備するもの

1. `data/sample_data.csv` を Excel で開く
2. 表全体をテーブルに変換して、テーブル名を **`sales_tbl`** にする

> テーブルへの変換方法は [workbook.md](workbook.md) の「準備するデータ」に書いてあります。

---

## 当日の進め方

| ステップ | 内容 | ファイル |
|----------|------|----------|
| 準備 | サンプルデータをExcelで開いてテーブルにする | [data/sample_data.csv](data/sample_data.csv) |
| 本編 | ワークブックに沿ってレッスンを進める | [workbook.md](workbook.md) |
| 練習 | 自分でコードを書いて試す | [exercises/](exercises/) |
| 確認 | 答えと解説を確認する | [solutions/](solutions/) |

---

## 練習問題一覧

| # | 内容 | ファイル |
|---|------|----------|
| 1 | 大阪支店の売上だけを表示する | [exercises/01_osaka_sales.md](exercises/01_osaka_sales.md) |
| 2 | B商品のデータだけを表示する | [exercises/02_b_product.md](exercises/02_b_product.md) |
| 3 | 売上が5000円以上のデータを表示する | [exercises/03_sales_5000.md](exercises/03_sales_5000.md) |
| 4 | 東京支店の件数を数える | [exercises/04_tokyo_count.md](exercises/04_tokyo_count.md) |
| 5 | A商品の平均売上を求める | [exercises/05_a_product_mean.md](exercises/05_a_product_mean.md) |
