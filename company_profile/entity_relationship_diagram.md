@startuml
title Enhanced ERD Diagram

' Style settings
skinparam backgroundColor #F5F5F5
skinparam entity {
  BackgroundColor #E3F2FD
  BorderColor #0288D1
  FontColor #01579B
}
skinparam entity {
  BackgroundColor #E1F5FE
  BorderColor #0288D1
}
skinparam title {
  BackgroundColor #0288D1
  FontColor #FFFFFF
}

' Entities
entity "Customer" as customer {
  *customer_id : INT
  *name : VARCHAR
  email : VARCHAR
  phone : VARCHAR
}

entity "Order" as order {
  *order_id : INT
  order_date : DATE
  amount : DECIMAL
}

entity "Product" as product {
  *product_id : INT
  *name : VARCHAR
  price : DECIMAL
}

entity "OrderItem" as orderItem {
  *order_item_id : INT
  quantity : INT
}

' Relationships
customer --o{ order : places
order --o{ orderItem : contains
product --o{ orderItem : includes

@enduml
