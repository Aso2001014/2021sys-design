```startuml
@startuml
package "ECサイト" as target_system {
entity "顧客マスタ" as customer <m_customers>{
        + customer_code [PK]
        --
        pass
        name
        address
        tel
        mail
        del_flag
        reg_date
        }
    entity "購入テーブル" as order <d_purchase>{
        + order_id [PK]
        --
        customer_code[FK]
        purchase_date
        total_price
        }
  entity "購入詳細テーブル" as orders <d_purchase_detail>{
        + order_id [PK]
        + detail_id[PK]
        --
        item_code[FK]
        price
        num
        }
   entity "商品マスタ" as item <m_items>{
        + item_code[PK]
        --
        item_name
        price
        category_id[FK]
        image
        detail
        del_flag
        reg_deta
        }
entity "カテゴリマスタ" as category <m_category>{
        + contegory_id[PK]
        --
        name
        reg_deta
            }
  }
  customer-left-{ order
  order-left-{ orders 
  
  
@enduml
```
