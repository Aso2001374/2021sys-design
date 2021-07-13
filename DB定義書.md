# DB定義書
## ER図
[ER図はこちら](https://github.com/Aso2001374/2021sys-design/blob/main/0705kadai.md "ER図はこちら")

## DBテーブルカラム詳細一覧

### 購入テーブル (d_purchase)
|和名|属性名|型|PK|NN|FK|
|:---|:-----|:--|:--|:--:|:--:|
|オーダーID|order id|bigint(20)|〇|〇|　|
|顧客コード|custmer_code|varchar(50)| |〇| |
|購入日|purchase_date|date| |〇|　|
|総額|total_price|int(11)| |〇||

### 購入詳細テーブル (d_purchase_detail)
|和名|属性名|型|PK|NN|FK|
|:---|:-----|:--|:--|:--:|:--:|
|購入詳細ID|detail_id|bigint(20)|〇|〇|　|
|オーダーID|order_id|bigint(20)|〇|〇|〇|
|商品コード|item_code|int(11)| |〇|　|
|価格|price|int(11)| |〇||
|数量|num|int(11)| |〇||

### 弁護士マスタ (m_lawyer)
|和名|属性名|型|PK|NN|FK|
|:---|:-----|:--|:--|:--:|:--:|
|弁護士登録番号|customer_code|int(5)|〇|〇|　|
|パスワード|pass|varchar(6)| |〇| |
|名前|name|varchar(20)| |〇|　|
|ふりがな|name|varchar(40)| |〇|　|
|住所|address|varchar(100)| |〇| |
|電話番号|tel|varchar(20)| |〇|　|
|メールアドレス|mail|varchar(50)| |〇| |
|削除フラグ|del_flag|int(1)| | |　|
|登録日|reg_date|date| |〇| |

### カテゴリマスタ (m_category)
|和名|属性名|型|PK|NN|FK|
|:---|:-----|:--|:--|:--:|:--:|
|カテゴリID|category_id|int(11)|〇|〇|　|
|カテゴリ名|name|varchar(20)| |〇| |
|登録日|reg_date|date| |〇| |

### 商品マスタ (m_items)
|和名|属性名|型|PK|NN|FK|
|:---|:-----|:--|:--|:--:|:--:|
|商品コード|item_code|int(11)|〇|〇|　|
|商品名|item_name|varchar(50)| |〇| |
|価格|price|int(11)| |〇|　|
|カテゴリID|category_id|int(11)| |〇| |
|画像ファイル名|image|varchar(200)| |〇|　|
|商品詳細説明|detail|varchar(500)|〇|〇| |
|削除フラグ|del_flag|int(1)|〇|〇|　|
|登録日|reg_date|date| |〇| |
