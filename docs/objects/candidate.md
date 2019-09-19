# candidate

Represents a candidate.

```` json
{
  "$schema": "http://json-schema.org/draft-04/schema#",
  "title": "ontime.js format: candidate",
  "description": "JSON schema for the data object candidate",
  "type": "object",
  "properties": {
    "id": {
      "description": "native id of the candidate",
      "type": "string"
    },
    "externalIds": {
      "description": "list of external ids for the candidate",
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
    "lastName": "string",
    "firstName": "string",
    "middleName": "string"
  }
}
````