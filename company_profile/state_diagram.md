@startuml
title State Diagram

' Define colors
skinparam backgroundColor #F0F4F8

' Define styles for states
skinparam state {
  BackgroundColor #E3F2FD
  BorderColor #2196F3
  FontColor #0D47A1
}

' Define styles for transitions
skinparam Arrow {
  Color #2196F3
  FontColor #0D47A1
}

' Define styles for title
skinparam title {
  BackgroundColor #BBDEFB
  BorderColor #64B5F6
  FontColor #0D47A1
}

' Define states and transitions
[*] --> Home

Home --> About : "About Us Link"
Home --> Services : "Services Link"
Home --> Contact : "Contact Link"
Home --> Portfolio : "Portfolio Link"

About --> Home : "Back to Home"
Services --> Home : "Back to Home"
Contact --> Home : "Back to Home"
Portfolio --> Home : "Back to Home"

@enduml
