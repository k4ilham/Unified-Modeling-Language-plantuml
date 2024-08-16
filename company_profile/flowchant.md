@startuml
title Contact Form Submission Process

' Style settings
skinparam backgroundColor #F0F8FF
skinparam title {
  BackgroundColor #4682B4
  FontColor #FFFFFF
}
skinparam actor {
  BackgroundColor #ADD8E6
  BorderColor #000080
  FontColor #000000
}
skinparam rectangle {
  BackgroundColor #E6E6FA
  BorderColor #0000FF
}
skinparam arrow {
  Color #0000FF
}

start
:Visitor Opens Contact Form;

if (Is Form Completed?) then (yes)
  :Submit Form;
  :Form Submission Recorded;
  :Send Confirmation Email to Visitor;
  :Notify Admin;
  :Notify Customer Support;
else (no)
  :Display Error Message;
endif

:End Process;
stop
@enduml
