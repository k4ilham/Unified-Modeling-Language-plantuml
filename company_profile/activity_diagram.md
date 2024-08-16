@startuml
title Contact Form Submission Process

' Customize colors for swimlanes
skinparam swimlane {
  BackgroundColor #F5F5F5
  BorderColor #B0B0B0
  BorderThickness 2
}

' Customize colors for activity boxes
skinparam activity {
  BackgroundColor #E0FFFF
  BorderColor #00CED1
  BorderThickness 1
}

' Customize colors for title
skinparam title {
  BackgroundColor #ADD8E6
  BorderColor #4682B4
  BorderThickness 2
  FontColor #000080
}

' Customize colors for note boxes
skinparam note {
  BackgroundColor #FFFFE0
  BorderColor #FFD700
}

start

:Visitor Browses Website;
:View Contact Page;

if (Wants to Submit Form?) then (Yes)
    :Fill Out Contact Form;
    :Submit Form;
    :Form Submission Recorded;
    fork
        :Notify Admin;
    fork again
        :Notify Customer Support;
    end fork
else (No)
    :Continue Browsing;
endif

fork
    :Admin Responds to Inquiry;
fork again
    :Customer Support Responds to Inquiry;
end fork

stop
@enduml
