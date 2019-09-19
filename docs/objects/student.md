# student

Represents a student.

```` json
{
  "$schema": "http://json-schema.org/draft-04/schema#",
  "title": "ontime.js format: student",
  "description": "JSON schema for the data object student",
  "type": "object",
  "properties": {
    "id": {
      "description": "native id of the student",
      "type": "string"
    },
    "externalIds": {
      "description": "list of external ids for the student",
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
      "description": "student code --remove",
      "type": "string"
    },
    "firstName": {
      "description": "student first name",
      "type": "string"
    },
    "middleName": {
      "description": "student middle name",
      "type": "string"
    },
    "lastName": {
      "description": "student last name",
      "type": "string"
    },
    "namePrefix": {
      "description": "student name suffix",
      "type": "string"
    },
    "nameSuffix": {
      "description": "student name suffix",
      "type": "string"
    },
    "nickName": {
      "description": "student nick name",
      "type": "string"
    },
    "maidenName": {
      "description": "student maiden name",
      "type": "string"
    },
    "studentNo": {
      "description": "student organisation number",
      "type": "string"
    },
    "studentTypeRef": {
      "description": "[native reference] student type",
      "type": "string"
    }
  }
}
````