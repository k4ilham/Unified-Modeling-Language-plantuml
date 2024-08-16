@startuml
object Homepage {
  + title: String
  + content: String
}

object AboutPage {
  + title: String
  + content: String
}

object ServicesPage {
  + title: String
  + servicesList: List<String>
}

object ContactPage {
  + title: String
  + contactForm: Form
}

object PortfolioPage {
  + title: String
  + projectsList: List<Project>
}

Homepage -- AboutPage : "Navigates to"
Homepage -- ServicesPage : "Navigates to"
Homepage -- ContactPage : "Navigates to"
Homepage -- PortfolioPage : "Navigates to"

@enduml
