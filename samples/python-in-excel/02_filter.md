# サンプル：条件で絞り込む

## 文字条件で絞り込む

```python
# 東京支店だけ
sales_tbl[sales_tbl["支店"] == "東京"]

# 大阪支店だけ
sales_tbl[sales_tbl["支店"] == "大阪"]

# A商品だけ
sales_tbl[sales_tbl["商品"] == "A商品"]

# B商品だけ
sales_tbl[sales_tbl["商品"] == "B商品"]
```

## 数値条件で絞り込む

```python
# 売上3000以上
sales_tbl[sales_tbl["売上"] >= 3000]

# 売上5000以上
sales_tbl[sales_tbl["売上"] >= 5000]
```

## 絞り込みと集計の組み合わせ

```python
# 東京支店の件数
sales_tbl[sales_tbl["支店"] == "東京"]["売上"].count()

# A商品の平均売上
sales_tbl[sales_tbl["商品"] == "A商品"]["売上"].mean()

# 大阪支店の売上合計
sales_tbl[sales_tbl["支店"] == "大阪"]["売上"].sum()
```

## 2つの条件を組み合わせる

```python
# 東京支店 かつ 売上3000以上
sales_tbl[(sales_tbl["支店"] == "東京") & (sales_tbl["売上"] >= 3000)]
```
