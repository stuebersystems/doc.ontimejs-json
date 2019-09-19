# course

Represents a course. A course is assigned to a subject and to one or more classes and can have one ore more lessons. In a lesson one or more teachers meet a class/students at a room.

```` json
{
  "$schema": "http://json-schema.org/draft-04/schema#",
  "title": "ontime.js format: course",
  "description": "JSON schema for the data object course",
  "type": "object",
  "properties": {
    "id": {
      "description": "native id of the course",
      "type": "string"
    },
    "externalIds": {
      "description": "list of external ids for the course",
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
    "title": {
      "description": "course name",
      "type": "string"
    },
    "description": {
      "description": "course description",
      "type": "string"
    },
    "remarks": {
      "description": "course remarks",
      "type": "string"
    },
    "url": {
      "description": "url",
      "type": "string"
    },
    "courseNo": {
      "description": "course number",
      "type": "string"
    },
    "courseTypeRef": {
      "description": "[native reference] course type",
      "type": "string"
    },
    "group": {
      "description": "group name",
      "type": "string"
    },
    "subjectRef": {
      "description": "[native reference] subject",
      "type": "string"
    },
    "roomRefs": {
      "description": "[native reference list] rooms",
      "type": "array",
      "items": {
        "type": "string"
      }
    },
    "studentRefs": {
      "description": "[native reference list] students",
      "type": "array",
      "items": {
        "type": "string"
      }
    },
    "teacherRefs": {
      "description": "[native reference list] teachers",
      "type": "array",
      "items": {
        "type": "string"
      }
    },
    "resourceRefs": {
      "description": "[native reference list] resources",
      "type": "array",
      "items": {
        "type": "string"
      }
    }
  }
}
````