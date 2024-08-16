@startuml
title Contact Form Submission Process

|Customer|
start
:Open Website;
:Navigate to Contact Page;
:Fill Out Contact Form;
:Submit Contact Form;

|Server|
:Receive Form;
:Validate Form;
:Process Form;
:Store Form Data;
:Send Confirmation;

|Customer|
:Receive Confirmation;
:Review Confirmation;

stop

' Customize colors for swimlanes
skinparam swimlane {
  BackgroundColor #F0F8FF
  BorderColor #4682B4
  BorderThickness 2
}

' Customize colors for activity boxes
skinparam activity {
  BackgroundColor #E6E6FA
  BorderColor #8A2BE2
  BorderThickness 1
}

' Customize colors for title
skinparam title {
  BackgroundColor #B0E0E6
  BorderColor #4682B4
  BorderThickness 2
  FontColor #000080
}

' Customize colors for note boxes
skinparam note {
  BackgroundColor #FFFFE0
  BorderColor #FFD700
}
@enduml
