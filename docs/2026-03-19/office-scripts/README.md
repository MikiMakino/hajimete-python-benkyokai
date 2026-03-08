# 2026-03-19 Office Scripts 勉強会

## テーマ：CSVデータを Office Scripts で整える

Excel で開いた CSV ファイルを、Office Scripts（TypeScript）を使って自動で整形する練習です。

---

## この日に学ぶこと

- Office Scripts の基本的な書き方
- セルの範囲を取得・操作する方法
- 書式設定（太字・背景色・中央揃え）
- 条件に合う行を削除する方法
- データをテーブルに変換する方法

---

## 練習問題

| # | 内容 | ファイル |
|---|------|----------|
| 1 | 1行目を見出しとして整える | [exercises/office-scripts/01_header_format.md](../../../exercises/office-scripts/01_header_format.md) |
| 2 | A列が空白の行を削除する | [exercises/office-scripts/02_delete_empty_rows.md](../../../exercises/office-scripts/02_delete_empty_rows.md) |
| 3 | データをテーブルに変換する | [exercises/office-scripts/03_convert_to_table.md](../../../exercises/office-scripts/03_convert_to_table.md) |

---

## 使い方

1. `data/` フォルダの `sample_data.csv` を Excel で開く
2. Excel のオートメーションタブ → 新しいスクリプト を開く
3. 練習問題を読んで、自分でコードを書いてみる
4. 詰まったらヒントを確認する
5. 解答は `samples/office-scripts/` にあります（まずは自分で挑戦！）

---

## サンプルデータ

[data/sample_data.csv](data/sample_data.csv)

受注データ（13行）です。途中に空白行が2か所含まれています。
