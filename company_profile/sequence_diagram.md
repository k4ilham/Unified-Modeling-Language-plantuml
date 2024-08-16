@startuml
title Sequence Diagram

' Define colors
skinparam backgroundColor #F8F9FA

' Define styles for actors
skinparam actor {
  BackgroundColor #E3F2FD
  BorderColor #2196F3
  FontColor #0D47A1
}

' Define styles for messages
skinparam Arrow {
  Color #2196F3
  FontColor #0D47A1
}

' Define styles for alt and else blocks
skinparam activity {
  BackgroundColor #E1BEE7
  BorderColor #AB47BC
  FontColor #6A1B9A
}

' Define styles for title
skinparam title {
  BackgroundColor #B3E5FC
  BorderColor #03A9F4
  FontColor #01579B
}

' Define actors
actor Visitor
actor CustomerSupport
actor Admin

' Define interactions
Visitor -> Website: Browse pages
Visitor -> Website: View Contact Page
Visitor -> ContactForm: Fill out form
Visitor -> Website: Submit form
Website -> Admin: Notify new form submission
Website -> CustomerSupport: Notify new inquiry

alt Admin handles
    Admin -> ContactForm: View form submission
    Admin -> Visitor: Respond to inquiry
else Customer Support handles
    CustomerSupport -> ContactForm: View form submission
    CustomerSupport -> Visitor: Respond to inquiry
end

@enduml
