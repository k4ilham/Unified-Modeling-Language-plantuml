@startuml
title Class Diagram for Company Profile Website

' Style settings
skinparam backgroundColor #F5F5F5
skinparam class {
  BackgroundColor #E6F7FF
  BorderColor #007ACC
  FontColor #333333
}
skinparam title {
  BackgroundColor #007ACC
  FontColor #FFFFFF
}

' Diagram content
class Visitor {
  + browseWebsite()
  + viewAboutUs()
  + viewServices()
  + viewPortfolio()
  + viewContactInfo()
  + submitContactForm()
}

class Admin {
  + manageUsers()
  + manageWebsiteSettings()
}

class ContentManager {
  + manageContent()
}

class CustomerSupport {
  + respondToInquiries()
}

class Website {
  + name
  + url
  + launchDate
  + services: List<Service>
  + content: List<Content>
}

class Service {
  + serviceName
  + description
  + price
  + showService()
}

class Content {
  + title
  + body
  + datePublished
  + updateContent()
}

class ContactForm {
  + name
  + email
  + message
  + submitForm()
}

Visitor --> Website : browse
Visitor --> ContactForm : submits
Admin --> Website : manages
ContentManager --> Content : updates
CustomerSupport --> ContactForm : responds
Website "1" -- "*" Service : contains
Website "1" -- "*" Content : hosts

@enduml
