``` uml
@startuml

!define MASTER_MARK_COLOR Orange 
!define TRANSACTION_MARK_COLOR DeepSkyBlue

skinparam class {
    '図の背景
    BackgroundColor Snow
    '図の枠
    BorderColor Black
    'リレーションの色
    ArrowColor Black
}

package "ECサイト" as target_system {

    entity "弁護士マスタ" as lawyer <m_lawyer> <<M,MASTER_MARK_COLOR>> {
        + customer_code [PK][FK]
        --
        pass
        name
        kana
        address
        posta_code
        office
        tel1
        tel2
        mail1
        mail2
        bank
        bank_number
        picture
        Prefectures_number
        consultation_code
        cash_code
        option_code
        del_flag
        reg_date
    }


    entity "レビューテーブル" as Review <d_Review> <<T,TRANSACTION_MARK_COLOR>> {
        + Review_id [PK][FK]
        + customer_code [PK]
        --
        date
    }


    entity "レビュー詳細テーブル" as Review-detail <d_Review-detail> <<T,TRANSACTION_MARK_COLOR>> {
        + Review_id [PK]
        + Review_detail-id[PK]
        + user_id[PK]
        --
        title
        Review
    }
    
    
    entity "条件マスタ" as conditions <d_conditions> <<M,MASTER_MARK_COLOR>> {
        + Prefectures_number [PK][FK]
        + consultation_code [PK][FK]
        + cash_code [PK][FK]
        + customer_code [PK][FK]
        + option_code [PK][FK]
        --
        Prefectures_name
        consultation_name
        cash_name
        name
        option_name
        del_flag
        reg_date
    }
    
    
    entity "顧客マスタ" as user <m_user> <<M,MASTER_MARK_COLOR>> {
        + user_id [PK]
        --
        pass
        name
        kana
        address
        posta_code
        tel1
        tel2
        mail1
        mail2
        del_flag
        reg_date
    }
    
     lawyer --r-- Review
     Review |-r-o{ Review-detail
     lawyer ||-r-|| conditions
 }   
@enduml
```
