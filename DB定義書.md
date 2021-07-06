# DB定義書
## ER図
[ER図はこちら](https://github.com/Aso2001374/2021sys-design/blob/main/0705kadai.md "ER図はこちら")

## DBテーブルカラム詳細一覧

d_purchase
|属性名|型|PK|NN|FK|
|-----|--|--|--|--|
|order id|bigint(20)|〇|〇|　|
|custmer_code|varchar(50)| |〇| |
|purchase_date|date| |〇|　|
|total_price|int(11)| |〇||

d_purchase_detail
|属性名|型|PK|NN|FK|
|-----|--|--|--|--|
|detail_id|bigint(20)|〇|〇|　|
|order_id|bigint(20)|〇|〇|〇|
|item_code|int(11)| |〇|　|
|price|int(11)| |〇||
|num|int(11)| |〇||

m_customers
|属性名|型|PK|NN|FK|
|-----|--|--|--|--|
|customer_code|varchar(50)|〇|〇|　|
|pass|varchar(50)| |〇| |
|name|varchar(20)| |〇|　|
|address|ivarchar(100)| |〇| |
|tel|varchar(20)| |〇|　|
|mail|varchar(50)| |〇| |
|del_flag|int(1)| | |　|
|reg_date|date| |〇| |

m_category
|属性名|型|PK|NN|FK|
|-----|--|--|--|--|
|category_id|int(11)|〇|〇|　|
|name|varchar(20)| |〇| |
|reg_date|date| |〇| |

m_items
|属性名|型|PK|NN|FK|
|-----|--|--|--|--|
|item_code|int(11)|〇|〇|　|
|item_name|varchar(50)| |〇| |
|price|int(11)| |〇|　|
|category_id|int(11)| |〇| |
|image|varchar(200)| |〇|　|
|detail|varchar(500)|〇|〇| |
|del_flag|int(1)|〇|〇|　|
|reg_date|date| |〇| |
