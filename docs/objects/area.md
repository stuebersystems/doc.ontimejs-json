# area

Represents a supervision area that means a location for a supervision.

```` json
{
  "$schema": "http://json-schema.org/draft-04/schema#",
  "title": "ontime.js format: area",
  "description": "JSON schema for the data object area",
  "type": "object",
  "properties": {
    "id": {
      "description": "native id of the area",
      "type": "string"
    },
    "externalIds": {
      "description": "list of external ids for the area",
      "type": "array",
      "items": {
        "type": "object",
        "properties": {
          "provider": {
            "description": "id provider",
            "type": "string"
          },
          "id": {
            "description": "id value",
            "type": "string"
          }
        }
      }
    },
    "code": {
      "description": "area code",
      "type": "string"
    },
    "description": {
      "description": "area description",
      "type": "string"
    }
  }
}
````