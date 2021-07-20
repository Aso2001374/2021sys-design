データベース詳細<br>
d_search
|属性名|型|PK|NN|FK|
|-----|--|--|--|--|
|customer_code|int(5)||||
|Prefectures_number|int(2)||||
|consultation_code|int(2)||| |
|cash_code|int(2)|||　|
|name_code|varchar(20)||||
|option_code|int(2)||||


m_conditions
|属性名|型|PK|NN|FK|
|-----|--|--|--|--|
|Prefectures_number|int(2)|〇|〇|〇|
|Prefectures|varchar(4)||〇||
|consultation_code|int(2)|〇|〇|〇|
|consultation_name|varchar(40)| |〇| |
|cash_code|int(2)|〇|〇|〇|
|cash_name|int(2)||〇||
|name_code|int(10)|〇|〇|〇|
|name|varchar(20)||〇||
|option_code|int(2)|〇|〇|〇|
|option_name|varchar(40)||〇||

m_lawyer
属性名|型|PK|NN|FK|
|-----|--|--|--|--|
|customer_code|int(5)|〇|〇|〇|
|pass|varchar(6)| |〇| |
|name|varchar(20)| |〇|　|
|kana|varchar(40)| |〇|　|
|address|varchar(100)| |〇| |
|posta_code|int(7)| |〇| |
|office|varchar(100)| |〇| |
|tel1|varchar(20)| |〇|　|
|tel2|varchar(20)| ||　|
|mail1|varchar(50)| |〇| |
|mail2|varchar(50)| || |
|bank|varchar(30)| |〇| |
|bank_number|int(7)| |〇| |
|picture|(webと同じやり方でimg)| |〇| |
|del_flag|int(1)|〇|〇|　|
|reg_date|date| |〇| |



m_user
|属性名|型|PK|NN|FK|
|-----|--|--|--|--|
|uer_id|int(8)|〇|〇|　|
|pass|varchar(6)| |〇| |
|name|varchar（20)| |〇| |
|kana|varchar（40)| |〇|　|
|address|varchar(100)| |〇| |
|posta_code|int(7)| |〇| |
|tel1|varchar(20)| |〇|　|
|tel2|varchar(20)| ||　|
|mail1|varchar(50)| |〇| |
|mail2|varchar(50)| || |
|del_flag|int(1)|〇|〇|　|
|reg_date|date| |〇| |
