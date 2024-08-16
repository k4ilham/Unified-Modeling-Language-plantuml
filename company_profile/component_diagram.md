@startuml
package "Frontend" {
    [Browser] --> [UI/Frontend]
}

package "Backend" {
    [UI/Frontend] --> [Web Server]
    [Web Server] --> [Application Logic]
    [Application Logic] --> [Database]
}

package "External Services" {
    [Payment Gateway]
    [Email Service]
}

[Browser] --> [Payment Gateway] : Process Payment
[Application Logic] --> [Email Service] : Send Email

@enduml
