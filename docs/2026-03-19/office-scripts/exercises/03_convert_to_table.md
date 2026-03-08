# 練習問題3：データをテーブルに変換する

## 問題

使用範囲全体をテーブルに変換してください。
先頭行は見出しとして扱います。

---

## ヒント

- `getUsedRange()` で使用範囲を取得する
- `workbook.addTable(range, hasHeaders)` でテーブルを作成できる
- テーブルに名前をつけておくと後から参照しやすい

```typescript
// テーブル作成の例
const table = workbook.addTable(usedRange, true);
table.setName("RawCsvTable");
```

---

## 確認ポイント

- [ ] フィルターがついている
- [ ] 見出し行が認識されている

---

## 解答

[solutions/03_convert_to_table.md](../solutions/03_convert_to_table.md)
