# 練習問題1：1行目を見出しとして整える

## 問題

`data/sample_data.csv` を Excel で開いた状態で、
1行目（ヘッダー行）を次の書式にしてください。

- 太字
- 背景色を薄い青（`#D9EAF7`）
- 文字を中央揃え

---

## ヒント

- アクティブシートを取得する
- `sheet.getRange("1:1")` で1行目全体を取得できる
- 書式は `getFormat()` から操作する

```typescript
// 書式操作の例
range.getFormat().getFont().setBold(true);
range.getFormat().getFill().setColor("#D9EAF7");
range.getFormat().setHorizontalAlignment(ExcelScript.HorizontalAlignment.center);
```

---

## 確認ポイント

- [ ] 1行目だけ見た目が変わる
- [ ] データ行はそのまま

---

## 解答

[solutions/01_header_format.md](../solutions/01_header_format.md)
