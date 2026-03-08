# 解答2：A列が空白の行を削除する

## コード

以下のコードを Office Scripts エディタに貼り付けて実行してください。

```typescript
function main(workbook: ExcelScript.Workbook) {
  // 今開いているシートを取得
  const sheet = workbook.getActiveWorksheet();

  // データが入っている範囲を取得
  const usedRange = sheet.getUsedRange();
  if (!usedRange) return;

  // 使用範囲の行数を取得
  const rowCount = usedRange.getRowCount();

  // 下の行から上に向かってチェック
  // 1行目はヘッダーなので2行目まで見る
  for (let row = rowCount; row >= 2; row--) {
    // A列の値を取得
    const value = sheet.getRange(`A${row}`).getValue();

    // A列が空白なら、その行を削除
    if (value === "" || value === null) {
      sheet.getRange(`${row}:${row}`).delete(ExcelScript.DeleteShiftDirection.up);
    }
  }
}
```

---

## 解説

### なぜ下から上にループするの？

上から削除していくと、行が詰まって**次に見るべき行がずれてしまいます**。

```
削除前：1行目（ヘッダー）、2行目（データ）、3行目（空白）、4行目（データ）
↓ 3行目を削除すると
削除後：1行目（ヘッダー）、2行目（データ）、3行目（データ）← 元の4行目が上に移動
```

下から見ていけば、削除しても上の行には影響しないので安全です。

### 使用範囲を取得する

```typescript
const usedRange = sheet.getUsedRange();
if (!usedRange) return;
const rowCount = usedRange.getRowCount();
```

`getUsedRange()` はデータが入っている範囲全体を返します。
何もない場合に備えて `if (!usedRange) return;` で早めに終了します。

### 空白かどうかを判定する

```typescript
if (value === "" || value === null) {
```

空文字 `""` と `null` の両方を空白として扱います。

### 行を削除する

```typescript
sheet.getRange(`${row}:${row}`).delete(ExcelScript.DeleteShiftDirection.up);
```

`${row}:${row}` は「その行全体」を表します（例：`"8:8"`）。
`DeleteShiftDirection.up` は削除後に下の行を上に詰めるという意味です。

---

## 少し変えて試してみよう

A列ではなくB列を基準にするには：

```typescript
const value = sheet.getRange(`B${row}`).getValue();
```
