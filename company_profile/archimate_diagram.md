@startuml
!define RECTANGLE class
!define COMPONENT rectangle

' Title and Styles
title Arsitektur Sistem Website
skinparam backgroundColor #F0F0F0
skinparam rectangle {
  BackgroundColor #D3EAF2
  BorderColor #007ACC
}
skinparam component {
  BackgroundColor #BFD3C1
  BorderColor #4F8A10
}
skinparam package {
  BackgroundColor #B0C4DE
  BorderColor #4682B4
  FontColor #FFFFFF
}

' Business Layer
package "Business Layer" as BL {
    [Customer] as Customer
    [Web Application] as WebApp

    Customer -down-> WebApp : "Accesses"
}

' Application Layer
package "Application Layer" as AL {
    COMPONENT "Web Server" as WebServer
    COMPONENT "Database Server" as DBServer

    WebServer -down-> WebApp : "Hosts"
    WebApp -right-> DBServer : "Queries"
}

' Technology Layer
package "Technology Layer" as TL {
    [Router] as Router
    [Network] as Network

    Router -right-> WebServer : "Routes Requests"
    Router -right-> DBServer : "Routes Queries"
    Network -down-> Router : "Connects"
}

' Relationships
Customer -down-> WebServer : "Requests Web Access"
WebServer -down-> Network : "Serves through"
DBServer -down-> Network : "Connects through"
@enduml
