@startgantt
title Project Timeline for Company Profile Website

' Style settings
skinparam backgroundColor #F0F8FF
skinparam gantt {
  BackgroundColor #FFFFFF
  BorderColor #0000FF
  BorderThickness 2
  Task {
    BackgroundColor #ADD8E6
    BorderColor #000080
    FontColor #000000
  }
  Dependency {
    Color #0000FF
  }
}

' Define the project tasks and their durations
[Project Planning] requires 5 days
[Requirements Gathering] requires 10 days
[Design Phase] requires 15 days
[Development Phase] requires 30 days
[Testing Phase] requires 10 days
[Deployment] requires 5 days
[Project Completion] requires 2 days

' Define task dependencies
[Project Planning] --> [Requirements Gathering]
[Requirements Gathering] --> [Design Phase]
[Design Phase] --> [Development Phase]
[Development Phase] --> [Testing Phase]
[Testing Phase] --> [Deployment]
[Deployment] --> [Project Completion]
@endgantt
