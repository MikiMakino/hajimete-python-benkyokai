# サンプル：Excel に保存する

```python
# DataFrame を Excel ファイルとして保存する
整理済み.to_excel("結果.xlsx", index=False)

# 特定の列だけ保存する
整理済み[["注文番号", "商品名", "金額"]].to_excel("金額一覧.xlsx", index=False)

# 絞り込んだ結果を保存する
整理済み[整理済み["金額"] >= 2000].to_excel("高額注文.xlsx", index=False)
```
