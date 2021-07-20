# DB定義書
## ER図
[ER図はこちら](https://github.com/Aso2001374/2021sys-design/blob/main/0705kadai.md "ER図はこちら")

## DBテーブルカラム詳細一覧

### 条件マスタ (m_conditions)
|和名|属性名|型|PK|NN|FK|
|:---|:-----|:--|:--|:--:|:--:|
|都道府県ナンバー|Prefectures_number|int(2)|〇|〇|〇|
|都道府県|Prefectures_name|varchar(4)||〇||
|相談項目ナンバー|consultation_code|int(2)|〇|〇|〇|
|相談項目|consultation_name|varchar(40)| |〇| |
|価格帯ナンバー|cash_code|int(2)|〇|〇|〇|
|価格帯|cash_name|int(2)||〇||
|弁護士登録番号|customer_code|int(5)|〇|〇|〇|
|弁護士名|name|varchar(20)||〇||
|オプションナンバー|option_code|int(2)|〇|〇|〇|
|オプション|option_name|varchar(40)||〇||
|削除フラグ|del_flag|int(1)|〇|〇|　|
|登録日|reg_date|date| |〇| |

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
|弁護士登録番号|customer_code|int(5)|〇|〇|〇|
|パスワード|pass|varchar(6)| |〇| |
|名前|name|varchar(20)| |〇|　|
|ふりがな|kana|varchar(40)| |〇|　|
|住所|address|varchar(100)| |〇| |
|郵便番号|posta_code|int(7)| |〇| |
|事務所|office|varchar(100)| |〇| |
|電話番号1|tel1|varchar(20)| |〇|　|
|電話番号2|tel2|varchar(20)| ||　|
|メールアドレス1|mail1|varchar(50)| |〇| |
|メールアドレス2|mail2|varchar(50)| || |
|銀行名|bank|varchar(30)| |〇| |
|口座番号|bank_number|int(7)| |〇| |
|顔写真|picture|(webと同じやり方でimg)| |〇| |
|削除フラグ|del_flag|int(1)|〇|〇|　|
|登録日|reg_date|date| |〇| |



### 顧客マスタ (m_user)
|和名|属性名|型|PK|NN|FK|
|:---|:-----|:--|:--|:--:|:--:|
|ユーザーID|user_id|int(8)|〇|〇|　|
|パスワード|pass|varchar(6)| |〇| |
|氏名|name|varchar（20)| |〇| |
|ふりがな|kana|varchar（40)| |〇|　|
|住所|address|varchar(100)| |〇| |
|郵便番号|posta_code|int(7)| |〇| |
|電話番号1|tel1|varchar(20)| |〇|　|
|電話番号2|tel2|varchar(20)| ||　|
|メールアドレス1|mail1|varchar(50)| |〇| |
|メールアドレス2|mail2|varchar(50)| || |
|削除フラグ|del_flag|int(1)|〇|〇|　|
|登録日|reg_date|date| |〇| |
