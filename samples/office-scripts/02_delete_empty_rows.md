# サンプル：A列が空白の行を削除する

```typescript
function main(workbook: ExcelScript.Workbook) {
  const sheet = workbook.getActiveWorksheet();
  const usedRange = sheet.getUsedRange();
  if (!usedRange) return;

  const rowCount = usedRange.getRowCount();

  for (let row = rowCount; row >= 2; row--) {
    const value = sheet.getRange(`A${row}`).getValue();

    if (value === "" || value === null) {
      sheet.getRange(`${row}:${row}`).delete(ExcelScript.DeleteShiftDirection.up);
    }
  }
}
```
