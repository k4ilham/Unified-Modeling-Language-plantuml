@startuml
title Object Diagram

' Define colors
skinparam backgroundColor #F5F5F5

' Define styles for objects
skinparam object {
  BackgroundColor #E0E0E0
  BorderColor #0000FF
  FontColor #000000
}

' Define styles for the title
skinparam title {
  BackgroundColor #ADD8E6
  BorderColor #4682B4
  FontColor #000080
}

' Define the objects with custom styles
object Homepage {
  + Title: String
  + Content: String
}

object AboutPage {
  + Title: String
  + Content: String
}

object ServicesPage {
  + Title: String
  + ServicesList: List<String>
}

object ContactPage {
  + Title: String
  + ContactForm: Form
}

object PortfolioPage {
  + Title: String
  + ProjectsList: List<Project>
}

' Define relationships
Homepage -- AboutPage : "Navigates to"
Homepage -- ServicesPage : "Navigates to"
Homepage -- ContactPage : "Navigates to"
Homepage -- PortfolioPage : "Navigates to"

@enduml
