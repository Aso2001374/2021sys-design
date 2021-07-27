データベース詳細<br>

m_conditions
|属性名|型|PK|NN|FK|
|-----|--|--|--|--|
|Prefectures_number|int(2)|〇|〇|〇|
|Prefectures_name|varchar(4)||〇||
|consultation_code|int(2)|〇|〇|〇|
|consultation_name|varchar(40)| |〇| |
|cash_code|int(2)|〇|〇|〇|
|cash_name|int(2)||〇||
|customer_code|int(5)|〇|〇|〇|
|name|varchar(20)||〇||
|option_code|int(2)|〇|〇|〇|
|option_name|varchar(40)||〇||
|del_flag|int(1)|〇|〇|　|
|reg_date|date| |〇| |


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
|picture|https://www.figma.com/file/EC6HJax9FH50cwnpwUmhDG/Untitled?node-id=29%3A2| |〇| |
|Prefectures_number|int(2)||〇||
|consultation_code|int(2)||〇||
|cash_code|int(2)||〇||
|option_code|int(2)||〇||
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



d_Review
|属性名|型|PK|NN|FK|
|-----|--|--|--|--|
|Review_id|int(10)|〇|〇|〇|
|customer_code|int(5)|〇|〇||
|date|date| |〇|〇|


d_Review-detail
|属性名|型|PK|NN|FK|
|-----|--|--|--|--|
|Review_id|int(10)|〇|〇|〇|
|Review_detail-id|int(10)|〇|〇||
|user_id|int(8)|〇|〇|　|
|title|varchar(100)| |〇||
|Review|varchar(1000)| |〇||
|del_flag|int(1)|〇|〇|　|
|reg_date|date| |〇| |
