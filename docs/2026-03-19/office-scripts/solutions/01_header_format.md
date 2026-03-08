# 解答1：1行目を見出しとして整える

## コード

以下のコードを Office Scripts エディタに貼り付けて実行してください。

```typescript
function main(workbook: ExcelScript.Workbook) {
  // 今開いているシートを取得
  const sheet = workbook.getActiveWorksheet();

  // 1行目全体を取得
  const headerRange = sheet.getRange("1:1");

  // 太字にする
  headerRange.getFormat().getFont().setBold(true);

  // 背景色を薄い青にする
  headerRange.getFormat().getFill().setColor("#D9EAF7");

  // 横方向を中央揃えにする
  headerRange.getFormat().setHorizontalAlignment(ExcelScript.HorizontalAlignment.center);
}
```

---

## 解説

### 1. シートを取得する

```typescript
const sheet = workbook.getActiveWorksheet();
```

今開いているシートを取得します。CSV は1枚しかないので、これで大丈夫です。

### 2. 1行目全体を取得する

```typescript
const headerRange = sheet.getRange("1:1");
```

`"1:1"` は「1行目全部」を意味します。
特定の列だけにしたい場合は `"A1:I1"` のように書きます。

### 3. 書式を変更する

```typescript
headerRange.getFormat().getFont().setBold(true);         // 太字
headerRange.getFormat().getFill().setColor("#D9EAF7");   // 背景色
headerRange.getFormat().setHorizontalAlignment(          // 中央揃え
  ExcelScript.HorizontalAlignment.center
);
```

`getFormat()` → `getFont()` や `getFill()` とつなげて、それぞれの書式を変更します。

---

## 少し変えて試してみよう

背景色を黄色にするには：

```typescript
headerRange.getFormat().getFill().setColor("#FFF2CC");
```

列幅を自動調整するには：

```typescript
sheet.getUsedRange().getFormat().autofitColumns();
```
