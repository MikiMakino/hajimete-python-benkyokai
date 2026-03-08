# 2026-03-19 Python 勉強会

## テーマ：2つの Excel ファイルをつないで、必要な情報を取り出す

VS Code を使いながら **Python（pandas）** の基本を体験します。
「受注データ」と「商品マスタ」を結合して整理する、実務に近い流れを体験します。

---

## この日に学ぶこと

- `# %%` 形式（セル実行）の使い方
- Excel ファイルを Python で読み込む
- 2つの表を結合する（VLOOKUP 相当）
- 必要な列だけ取り出す
- 計算列を追加する
- 結合できなかったデータを確認する

---

## 準備するもの

| ファイル | 場所 |
|----------|------|
| VS Code（インストール済み） | — |
| Python 拡張機能（Jupyter） | VS Code に追加 |
| `受注データ.xlsx` | [data/受注データ.xlsx](data/受注データ.xlsx) |
| `商品マスタ.xlsx` | [data/商品マスタ.xlsx](data/商品マスタ.xlsx) |

> `data/` フォルダの Excel ファイルを `workbook.py` と**同じフォルダ**に置いて使ってください。

---

## 当日の進め方

| ステップ | 内容 | ファイル |
|----------|------|----------|
| 準備 | Excel ファイルをダウンロードして配置 | [data/](data/) |
| 本編 | ワークブックに沿ってレッスンを進める | [workbook.py](workbook.py) |
| 練習 | 自分でコードを書いて試す | [exercises/](exercises/) |
| 確認 | 答えと解説を確認する | [solutions/](solutions/) |

---

## レッスン構成

| レッスン | 内容 |
|----------|------|
| 準備編 | 環境確認・print・変数 |
| Lesson 1 | `# %%` 形式に慣れる |
| Lesson 2 | pandas を読み込む |
| Lesson 3 | Excel ファイルを読み込む |
| Lesson 4 | 中身を確認する（head / shape / dtypes） |
| Lesson 5 | 結合キーを確認する |
| Lesson 6 | 型と表記を整える（前処理） |
| Lesson 7 | 2つの表を結合する（merge） |
| Lesson 8 | 結合結果を確認する |
| Lesson 9 | 必要な列だけ取り出す |
| Lesson 10 | 計算列を追加する |
| Lesson 11 | 結合できなかったデータを確認する |
| Lesson 12 | 腕試し練習（4問） |
| Lesson 13 | 振り返り |

---

## 練習問題一覧

| # | 内容 | ファイル |
|---|------|----------|
| 1 | 指定カテゴリのデータだけ取り出す | [exercises/01_category_filter.md](exercises/01_category_filter.md) |
| 2 | 金額が2000円以上の注文だけ取り出す | [exercises/02_amount_filter.md](exercises/02_amount_filter.md) |
| 3 | 商品コードごとの合計金額を集計する | [exercises/03_groupby.md](exercises/03_groupby.md) |
| 4 | 整理済みデータを Excel に保存する | [exercises/04_export_excel.md](exercises/04_export_excel.md) |
