@startuml
actor Visitor
actor CustomerSupport
actor Admin

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
