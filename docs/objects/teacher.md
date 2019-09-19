# teacher

Represents a teacher.

```` json
{
  "$schema": "http://json-schema.org/draft-04/schema#",
  "title": "ontime.js format: teacher",
  "description": "JSON schema for the data object teacher",
  "type": "object",
  "properties": {
    "id": {
      "description": "native id of the teacher",
      "type": "string"
    },
    "externalIds": {
      "description": "list of external ids for the teacher",
      "type": "array",
      "items": {
        "provider": {
          "description": "id provider",
          "type": "string"
        },
        "id": {
          "description": "id value",
          "type": "string"
        }
      }
    },
    "code": {
      "description": "teacher code",
      "type": "string"
    },
    "firstName": {
      "description": "short teacher description",
      "type": "string"
    },
    "middleName": {
      "description": "long teacher description",
      "type": "string"
    },
    "lastName": {
      "description": "long teacher description",
      "type": "string"
    },
    "namePrefix": {
      "description": "long teacher description",
      "type": "string"
    },
    "nameSuffix": {
      "description": "long teacher description",
      "type": "string"
    },
    "nickName": {
      "description": "long teacher description",
      "type": "string"
    },
    "maidenName": {
      "description": "long teacher description",
      "type": "string"
    },
    "color": {
      "description": "teacher color",
      "type": "integer"
    },
    "teacherNo": {
      "description": "[native reference] teacher organisation number",
      "type": "string"
    },
    "teacherTypeRef": {
      "description": "[native reference] teacher type",
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