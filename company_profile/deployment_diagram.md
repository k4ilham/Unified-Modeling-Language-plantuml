@startuml
title System Architecture Diagram

' Style settings
skinparam backgroundColor #F0F0F0
skinparam node {
  BackgroundColor #E0F7FA
  BorderColor #00796B
}
skinparam rectangle {
  BackgroundColor #E8F5E9
  BorderColor #1B5E20
}
skinparam class {
  BackgroundColor #FFFFFF
  BorderColor #009688
  FontColor #333333
}
skinparam title {
  BackgroundColor #00796B
  FontColor #FFFFFF
}

' Diagram content
node "Web Server" {
  [Web Application] << (S, #FFAAAA) >>
}

node "Database Server" {
  [Database] << (D, #FFDDDD) >>
}

rectangle "Client Browser" {
  [User Interface] << (U, #FFFFAA) >>
}

[User Interface] --> [Web Application] : "HTTP Requests"
[Web Application] --> [Database] : "Database Queries"

@enduml
