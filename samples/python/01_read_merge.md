# サンプル：Excel を読み込んで結合する

```python
import pandas as pd

# Excel ファイルを読み込む
受注 = pd.read_excel("受注データ.xlsx")
マスタ = pd.read_excel("商品マスタ.xlsx")

# 中身を確認する
受注.head()
print(受注.shape)
print(受注.dtypes)

# キー列を確認する
print(受注["商品コード"].unique())
print(マスタ["商品コード"].unique())

# 型と表記を整える（前処理）
受注["商品コード"] = 受注["商品コード"].astype(str).str.strip()
マスタ["商品コード"] = マスタ["商品コード"].astype(str).str.strip()

# 2つの表を結合する（VLOOKUP相当）
結合済み = pd.merge(受注, マスタ, on="商品コード", how="left")

# 欠損を確認する
print(結合済み.isna().sum())

# 必要な列だけ取り出す
必要列 = ["注文日", "注文番号", "商品コード", "商品名", "単価", "数量", "カテゴリ"]
整理済み = 結合済み[必要列].copy()

# 計算列を追加する
整理済み["金額"] = 整理済み["数量"] * 整理済み["単価"]
```
