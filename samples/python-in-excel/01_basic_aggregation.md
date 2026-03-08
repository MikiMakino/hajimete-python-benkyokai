# サンプル：基本集計

`sales_tbl` という名前のテーブルに対して使うコードです。

```python
# 合計
sales_tbl["売上"].sum()

# 平均
sales_tbl["売上"].mean()

# 最大値
sales_tbl["売上"].max()

# 最小値
sales_tbl["売上"].min()

# 件数
sales_tbl["売上"].count()
```

列名を変えれば、他の列にも同じ操作が使えます。

```python
# 数量の合計
sales_tbl["数量"].sum()

# 単価の平均
sales_tbl["単価"].mean()
```
