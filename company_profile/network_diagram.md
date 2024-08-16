@startuml
title System Architecture Diagram

' Style settings
skinparam backgroundColor #F0F8FF
skinparam title {
  BackgroundColor #4682B4
  FontColor #FFFFFF
  FontSize 16
}
skinparam node {
  BackgroundColor #E6E6FA
  BorderColor #0000FF
  FontColor #000000
}
skinparam arrow {
  Color #0000FF
}

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
