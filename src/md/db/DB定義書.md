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

### 顧客マスタ(m_customers)
|和名|属性名(カラム名)|型|PK|NN|FK|
|:--|:--|:--|:--|:--|:--|
|顧客コード|customer_code|varchar(50)|○|○||
|パスワード|pass|varchar(50)|○|○|○|
|氏名|name|varchar(20)||○||
|住所|address|varchar(100)||○||
|電話番号|tel|varchar(20)||○||
|メールアドレス|mail|varchar(100)||○||
|消去フラグ|del_flag|int(1)||||
|登録日|reg_date|date||○||

### カテゴリマスタ (m_category)
|和名|属性名|型|PK|NN|FK|
|:--|:--|:--|:--|:--|:--|
|カテゴリID|category_id|int(11)|○|○||
|氏名|name|varchar(20)||○||
|登録日|reg_date|date||○|| 

### 商品マスタ　（m_items）
|和名|属性名|型|PK|NN|FK|
|:--|:--|:--|:--|:--|:--|
|商品名|item_code|int(11)|○|○||
|価格|item_name|varchar(50)||○|| 
|カテゴリ|price|int(11)||○||
|画像ファイル|category_id|int(11)||○|○|
|商品詳細説明|image|varchar(200)||○||
|消去フラグ|detail|varchar(500)|||| 
|登録日|del_flag|int(11)||||
|氏名|reg_date|date ||○||

