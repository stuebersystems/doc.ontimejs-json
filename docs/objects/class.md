# class

Represents a class.

```` json
{
  "$schema": "http://json-schema.org/draft-04/schema#",
  "title": "ontime.js format: class",
  "description": "JSON schema for the data object class",
  "type": "object",
  "properties": {
    "id": {
      "description": "native id of the class",
      "type": "string"
    },
    "externalIds": {
      "description": "list of external ids for the class",
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
      "description": "class code",
      "type": "string"
    },
    "description": {
      "description": "class description",
      "type": "string"
    },
    "school": {
      "description": "school ID",
      "type": "string"
    },
    "institution": {
      "description": "institution ID",
      "type": "string"
    },
    "color": {
      "description": "class color",
      "type": "integer"
    },
    "classTypeRef": {
      "description": "[native reference] class type",
      "type": "string"
    },
    "studentRefs": {
      "description": "[native reference list] students",
      "type": "array",
      "items": {
        "type": "string"
      }
    },
    "roles": {
      "description": "list of persons with specific roles within the class",
      "type": "object",
      "properties": {
        "students": {
          "description": "list of students",
          "type": "array",
          "items": {
            "type": "object",
            "properties": {
              "refId": {
                "description": "[native reference] student",
                "type": "string"
              },
              "roleRef": {
                "description": "[native reference] studentClassRole",
                "type": "string"
              }
            }
          }
        },
        "teachers": {
          "description": "list of teachers",
          "type": "array",
          "items": {
            "type": "object",
            "properties": {
              "refId": {
                "description": "[native reference] teacher",
                "type": "string"
              },
              "roleRef": {
                "description": "[native reference] teacherClassRole",
                "type": "string"
              }
            }
          }
        }
      }
    },
    "teamRefs": {
      "description": "[native reference list] teams",
      "type": "array",
      "items": {
        "type": "string"
      }
    }
  }
}
````