@startuml

class "John Smith\n(CEO)" as ceo
class "Alice Johnson\n(CTO)" as cto
class "Robert Brown\n(CFO)" as cfo
class "Sarah White\nHead of Engineering" as engHead
class "Michael Green\nHead of Sales" as salesHead
class "Emily Davis\nHead of Marketing" as mktHead
class "David Wilson\nLead Engineer" as leadEng
class "Linda Martinez\nSenior Engineer" as seniorEng
class "James Taylor\nEngineer" as engineer
class "Karen Lee\nSales Manager" as salesMgr
class "Tom Clark\nSalesperson" as salesperson
class "Nancy Lewis\nMarketing Manager" as mktMgr
class "Sophia Young\nMarketing Specialist" as mktSpec

ceo -- cto : "Reports to"
ceo -- cfo : "Reports to"

cto -- engHead : "Reports to"
cfo -- salesHead : "Reports to"
cfo -- mktHead : "Reports to"

engHead -- leadEng : "Reports to"
engHead -- seniorEng : "Reports to"
leadEng -- engineer : "Manages"
seniorEng -- engineer : "Manages"

salesHead -- salesMgr : "Reports to"
salesMgr -- salesperson : "Manages"

mktHead -- mktMgr : "Reports to"
mktMgr -- mktSpec : "Manages"

@enduml
