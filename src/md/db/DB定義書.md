# DB定義書
## ER図
[ER図](https://github.com/Aso2001014/2021sys-design/blob/main/kadai23.md "ER図はこちら" )

# DBテーブルテーブルカラム詳細

### 購入テーブル　(d_purchae)
|和名|属性名（カラム名）|型|PK|NN|FK|
|:--|:--|:--|:--|:--|:--|
|オーダーID|order_id|bigint(20|○|AUTO_INCREMENT|○||
|購入コード|customer_code|varchar(50)||○||
|購入日|purchase_date|date||○||
|総額|total_price|int(11)||○||

### 　購入詳細 (d_punchase_detail)
|和名|属性名|型|PK|NN|FK|
|:--|:--|:--|:--|:--|:--|
|オーダー詳細ID|detail_id|bigint(20)|○|○||
|オーダーID|order_id|bigint(20)|○|○|○|
|商品コード|item_code|int(11)||○||
|価格|price|int(11)||○|| 
|数量|num|int(11)||○|| 

### 商品マスタ(m_customers)
|和名|属性名(カラム名)|型|PK|NN|FK|
|:--|:--|:--|:--|:--|:--|
|customer_code|varchar(50)|○|○||
|pass|varchar(50)|○|○|○|
|name|varchar(20)||○||
|address|varchar(100)||○||
|tel|varchar(20)||○||
|mail|varchar(100)||○||
|del_flag|int(1)||||
|reg_date|date||○||

### カテゴリマスタ (m_category)
|属性名|型|PK|NN|FK|
|:--|:--|:--|:--|:--|
|category_id|int(11)|○|○||
|name|varchar(20)||○||
|reg_date|date||○|| 

### 商品マスタ　（m_items）
|属性名|型|PK|NN|FK|
|:--|:--|:--|:--|:--|
|item_code|int(11)|○|○||
|item_name|varchar(50)||○|| 
|price|int(11)||○||
|category_id|int(11)||○|○|
|image|varchar(200)||○||
|detail|varchar(500)|||| 
|del_flag|int(11)||||
|reg_date|date ||○||

