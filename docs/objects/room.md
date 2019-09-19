# room

Represents a room.

```` json
{
  "$schema": "http://json-schema.org/draft-04/schema#",
  "title": "ontime.js format: room",
  "description": "JSON schema for the data object room",
  "type": "object",
  "properties": {
    "id": {
      "description": "native id of the room",
      "type": "string"
    },
    "externalIds": {
      "description": "list of external ids for the room",
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
      "description": "room code",
      "type": "string"
    },
    "description": {
      "description": "short room description",
      "type": "string"
    },
    "color": {
      "description": "room color",
      "type": "integer"
    },
    "roomTypeRef": {
      "description": "[native reference] room type",
      "type": "string"
    },
    "buildingRef": {
      "description": "[native reference] building",
      "type": "string"
    },
    "teamRefs": {
      "description": "[code reference list] teams",
      "type": "array",
      "items": {
        "type": "string"
      }
    },
    "equipment": {
      "description": "list of available resource types",
      "type": "array",
      "items": {
        "resourceTypeRef": {
          "description": "[native ref] resource type",
          "type": "string"
        },
        "resourceCapacity": {
          "description": "resource capacity",
          "type": "integer"
        }
      }
    }
  }
}
````