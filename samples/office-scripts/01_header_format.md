# サンプル：1行目を見出しとして整える

```typescript
function main(workbook: ExcelScript.Workbook) {
  const sheet = workbook.getActiveWorksheet();
  const headerRange = sheet.getRange("1:1");

  headerRange.getFormat().getFont().setBold(true);
  headerRange.getFormat().getFill().setColor("#D9EAF7");
  headerRange.getFormat().setHorizontalAlignment(ExcelScript.HorizontalAlignment.center);
}
```
