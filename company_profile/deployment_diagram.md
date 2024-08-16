@startuml
!define RECTANGLE class

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
