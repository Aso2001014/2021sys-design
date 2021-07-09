###データベース詳細
**d_punchase**
|属性名|型|PK|NN|FK|
|:--|:--|:--|:--|:--|
|order_id|bigint(20|○|AUTO_INCREMENT|○||
|customer_code|varchar(50)||○||
|purchase_date|date||○||
|total_price|int(11)||○||

**d_punchase_detail**
|属性名|型|PK|NN|FK|
|:--|:--|:--|:--|:--|
|detail_id|bigint(20)|○|○||
|order_id|bigint(20)|○|○|○|
|item_code|int(11)||○||
|price|int(11)||○|| 
|num|int(11)||○|| 

**m_customers**
|属性名|型|PK|NN|FK|
|:--|:--|:--|:--|:--|
|customer_code|varchar(50)|○|○||
|pass|varchar(50)|○|○|○|
|name|varchar(20)||○||
|address|varchar(100)||○||
|tel|varchar(20)||○||
|mail|varchar(100)||○||
|del_flag|int(1)||||
|reg_date|date||○||

**m_category**
|属性名|型|PK|NN|FK|
|:--|:--|:--|:--|:--|
|category_id|int(11)|○|○||
|name|varchar(20)||○||
|reg_date|date||○|| 

**m_items** 
|属性名|型|PK|NN|FK|
|:--|:--|:--|:--|:--|
  item_code` int(11) NOT NULL DEFAULT '0', 

  `item_name` varchar(50) NOT NULL, 

  `price` int(11) NOT NULL, 

  `category_id` int(11) NOT NULL, 

  `image` varchar(200) NOT NULL, 

  `detail` varchar(500) DEFAULT NULL, 

  `del_flag` int(11) DEFAULT NULL, 

  `reg_date` date NOT NULL, 

  PRIMARY KEY (`item_code`), 

  FOREIGN KEY PK_category(category_id) REFERENCES m_category(category_id) 

) 
