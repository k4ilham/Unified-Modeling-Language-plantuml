@startuml
== User Request ==
User -> WebApp : Request Page
WebApp -> Database : Query Data
Database --> WebApp : Return Data
WebApp --> User : Display Page

@enduml
