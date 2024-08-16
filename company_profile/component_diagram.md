@startuml
title System Architecture Diagram

' Style settings
skinparam backgroundColor #F9F9F9
skinparam package {
  BackgroundColor #E0E0E0
  BorderColor #009688
}
skinparam class {
  BackgroundColor #FFFFFF
  BorderColor #007ACC
  FontColor #333333
}
skinparam title {
  BackgroundColor #007ACC
  FontColor #FFFFFF
}

' Diagram content
package "Frontend" {
    [Browser] as Browser
    [UI/Frontend] as UIFrontend
    Browser --> UIFrontend
}

package "Backend" {
    [Web Server] as WebServer
    [Application Logic] as AppLogic
    [Database] as Database

    UIFrontend --> WebServer
    WebServer --> AppLogic
    AppLogic --> Database
}

package "External Services" {
    [Payment Gateway] as PaymentGateway
    [Email Service] as EmailService
}

Browser --> PaymentGateway : Process Payment
AppLogic --> EmailService : Send Email

@enduml
