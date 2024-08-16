@startuml
!define RECTANGLE class

node "Client Browser" as Browser {
  [User Device]
}

node "Web Server" as WebServer {
  [Web Application Server]
}

node "Database Server" as DBServer {
  [Database]
}

node "Router" as Router {
  [Network Router]
}

Router --> WebServer : "HTTP"
WebServer --> DBServer : "Database Queries"
Browser --> Router : "Internet"
Router --> Browser : "HTTP Response"

@enduml
