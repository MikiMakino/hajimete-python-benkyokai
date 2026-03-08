# 解答3：データをテーブルに変換する

## コード

以下のコードを Office Scripts エディタに貼り付けて実行してください。

```typescript
function main(workbook: ExcelScript.Workbook) {
  // 今開いているシートを取得
  const sheet = workbook.getActiveWorksheet();

  // 使用範囲を取得
  const usedRange = sheet.getUsedRange();
  if (!usedRange) return;

  // 使用範囲をテーブルに変換（true = 先頭行を見出しとして扱う）
  const table = workbook.addTable(usedRange, true);

  // テーブルに名前をつける
  table.setName("RawCsvTable");
}
```

---

## 解説

### テーブルにすると何がいいの？

ただのセルの集まりから、Excel が「表」として認識する状態になります。

- 見出しにフィルターがつく
- 並べ替えがしやすくなる
- Power Automate などの後続処理で扱いやすくなる

### 使用範囲をテーブルに変換する

```typescript
const table = workbook.addTable(usedRange, true);
```

- 第1引数：テーブルにする範囲（今回は使用範囲全体）
- 第2引数：`true` = 先頭行を見出しとして扱う

### テーブルに名前をつける

```typescript
table.setName("RawCsvTable");
```

名前をつけておくと、後からスクリプトで参照しやすくなります。
ただし、同じ名前のテーブルがすでにある場合はエラーになるので注意してください。

---

## 少し変えて試してみよう

テーブル名を変えるには：

```typescript
table.setName("SalesData");
```
