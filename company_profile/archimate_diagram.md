@startuml
!define RECTANGLE class
!define COMPONENT rectangle

' Business Layer
package "Business Layer" {
    [Customer] as Customer
    [Web Application] as WebApp

    Customer -down-> WebApp : "Accesses"
}

' Application Layer
package "Application Layer" {
    COMPONENT "Web Server" as WebServer
    COMPONENT "Database Server" as DBServer

    WebServer -down-> WebApp : "Hosts"
    WebApp -right-> DBServer : "Queries"
}

' Technology Layer
package "Technology Layer" {
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
