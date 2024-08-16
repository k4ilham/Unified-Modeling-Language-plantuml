@startuml
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
