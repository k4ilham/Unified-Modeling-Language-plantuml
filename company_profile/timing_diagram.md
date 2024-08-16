@startuml
title Timing Diagram

' Define colors
skinparam backgroundColor #F5F5F5

' Define styles for participants
skinparam participant {
  BackgroundColor #E0F2F1
  BorderColor #004D40
  FontColor #004D40
}

' Define styles for messages
skinparam Arrow {
  Color #00796B
  FontColor #004D40
}

' Define styles for title
skinparam title {
  BackgroundColor #B2DFDB
  BorderColor #004D40
  FontColor #004D40
}

' Define participants and interactions
== User Request ==
User -> WebApp : Request Page
WebApp -> Database : Query Data
Database --> WebApp : Return Data
WebApp --> User : Display Page

@enduml
