@startuml
title Usecase Diagram

' Define colors
skinparam backgroundColor #F4F6F9

' Define styles for actors
skinparam actor {
  BackgroundColor #E0E0E0
  BorderColor #9E9E9E
  FontColor #424242
}

' Define styles for use cases
skinparam usecase {
  BackgroundColor #D0E1F9
  BorderColor #1E88E5
  FontColor #0D47A1
}

' Define styles for arrows
skinparam Arrow {
  Color #1E88E5
  FontColor #0D47A1
}

' Define styles for title
skinparam title {
  BackgroundColor #C5CAE9
  BorderColor #3F51B5
  FontColor #1A237E
}

' Define actors and use cases
actor "Visitor" as visitor
actor "Admin" as admin
actor "Content Manager" as contentManager
actor "Customer Support" as support

usecase "Browse Website" as UC1
usecase "View About Us" as UC2
usecase "View Services" as UC3
usecase "View Portfolio" as UC4
usecase "View Contact Information" as UC5
usecase "Submit Contact Form" as UC6
usecase "Login" as UC7
usecase "Manage Content" as UC8
usecase "Manage Users" as UC9
usecase "Respond to Inquiries" as UC10
usecase "Manage Website Settings" as UC11

visitor --> UC1
visitor --> UC2
visitor --> UC3
visitor --> UC4
visitor --> UC5
visitor --> UC6
visitor --> UC7

contentManager --> UC8
admin --> UC9
admin --> UC11
support --> UC10

UC6 --> UC10 : <<includes>>
UC9 --> UC7 : <<extends>>
UC8 --> UC11 : <<includes>>

@enduml
