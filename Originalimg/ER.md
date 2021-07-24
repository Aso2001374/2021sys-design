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
    
    
    entity "マスタ" as items <d_Review-detail> <<M,MASTER_MARK_COLOR>> {
        + item_code [PK]
        --
        item_name
        price
        category_id
        image
        detail
        del_flag
        reg_date
    }
    
    
    entity "カテゴリマスタ" as category <m_category> <<M,MASTER_MARK_COLOR>> {
        + category_id [PK]
        --
        name
        reg_date
    }
    
     customer |o-r-o{ purchase
     purchase ||-r-|{ purchase_detail
     purchase_detail }-d-|| items
     items }o-l-|| category
 
 }   
@enduml
```
