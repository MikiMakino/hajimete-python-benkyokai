# サンプル：データをテーブルに変換する

```typescript
function main(workbook: ExcelScript.Workbook) {
  const sheet = workbook.getActiveWorksheet();
  const usedRange = sheet.getUsedRange();
  if (!usedRange) return;

  const table = workbook.addTable(usedRange, true);
  table.setName("RawCsvTable");
}
```
