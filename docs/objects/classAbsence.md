# classAbsence

Represents a class absence.

```` json
{
  "$schema": "http://json-schema.org/draft-04/schema#",
  "title": "ontime.js format: classAbsence",
  "description": "JSON schema for the data object classAbsence",
  "type": "object",
  "properties": {
    "id": {
      "description": "native id of absence",
      "type": "string"
    },
    "externalIds": {
      "description": "list of external ids for the absence",
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
    "classRef": {
      "description": "[native reference] class",
      "type": "string"
    },
    "startDate": {
      "description": "start date of absence",
      "type": "string"
    },
    "endDate": {
      "description": "end date of absence",
      "type": "string"
    },
    "startTime": {
      "description": "start time of absence",
      "type": "string"
    },
    "endTime": {
      "description": "end time of absence",
      "type": "string"
    },
    "reasonRef": {
      "description": "[native reference] classAbsentReasons",
      "type": "string"
    },
    "note": {
      "description": "remarks",
      "type": "string"
    }
  }
}
````