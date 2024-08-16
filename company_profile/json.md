@startjson
' Define styles for highlighting
<style>
  .highlight1 {
    BackgroundColor #008000
    FontColor #FFFFFF
    FontStyle italic
  }
  .highlight2 {
    BackgroundColor #FF0000
    FontColor #FFFFFF
    FontStyle bold
  }
  .default {
    BackgroundColor #F0F8FF
    BorderColor #000000
  }
</style>

' JSON data with styling
#highlight "lastName" <<highlight1>>
#highlight "address" / "city" <<highlight1>>
#highlight "phoneNumbers" / "0" / "number" <<highlight2>>
{
  "firstName": "John",
  "lastName": "Smith",
  "isAlive": true,
  "age": 28,
  "address": {
    "streetAddress": "21 2nd Street",
    "city": "New York",
    "state": "NY",
    "postalCode": "10021-3100"
  },
  "phoneNumbers": [
    {
      "type": "home",
      "number": "212 555-1234"
    },
    {
      "type": "office",
      "number": "646 555-4567"
    }
  ],
  "children": [],
  "spouse": null
}
@endjson
