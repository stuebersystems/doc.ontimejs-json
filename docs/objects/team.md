# team

Represents a team (e.g. department, faculty).

```` json
{
  "$schema": "http://json-schema.org/draft-04/schema#",
  "title": "ontime.js format: team",
  "description": "JSON schema for the data object team",
  "type": "object",
  "properties": {
    "id": {
      "description": "native id of the team",
      "type": "string"
    },
    "externalIds": {
      "description": "list of external ids for the team",
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
      "description": "team code",
      "type": "string"
    },
    "description": {
      "description": "team description",
      "type": "string"
    },
    "color": {
      "description": "team color",
      "type": "integer"
    }
  }
}
````

