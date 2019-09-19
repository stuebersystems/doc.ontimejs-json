# subject

Represents a subject.

```` json
{
  "$schema": "http://json-schema.org/draft-04/schema#",
  "title": "ontime.js format: subject",
  "description": "JSON schema for the data object subject",
  "type": "object",
  "properties": {
    "id": {
      "description": "native id of the subject",
      "type": "string"
    },
    "externalIds": {
      "description": "list of external ids for the subject",
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
      "description": "subject code",
      "type": "string"
    },
    "description": {
      "description": "subject description",
      "type": "string"
    },
    "color": {
      "description": "subject color",
      "type": "integer"
    },
    "subjectTypeRef": {
      "description": "[native reference] subject type",
      "type": "string"
    },
    "teamRefs": {
      "description": "[code reference list] teams",
      "type": "array",
      "items": {
        "type": "string"
      }
    }
  }
}
````