# 練習問題2：A列が空白の行を削除する

## 問題

`data/sample_data.csv` を Excel で開いた状態で、
A列が空白の行を削除してください。

---

## ヒント

- `getUsedRange()` で使用範囲を取得する
- セルの値を読んで空白か判定する
- **下から上に向かって**ループする（上から消すと行がずれる）

```typescript
// 下から上へのループ例
for (let i = rowCount; i >= 2; i--) {
  // i行目のA列を確認する
}

// 行削除の例
sheet.getRange(`${i}:${i}`).delete(ExcelScript.DeleteShiftDirection.up);
```

---

## 確認ポイント

- [ ] 途中にあった空白行が消える
- [ ] 表が詰まって並ぶ

---

## 解答

[solutions/02_delete_empty_rows.md](../solutions/02_delete_empty_rows.md)
