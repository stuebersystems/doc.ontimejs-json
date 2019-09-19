# building

Represents a building. Every room can have assigned a building.

```` json
{
  "$schema": "http://json-schema.org/draft-04/schema#",
  "title": "ontime.js format: building",
  "description": "JSON schema for the data object building",
  "type": "object",
  "properties": {
    "id": {
      "description": "native id of the building",
      "type": "string"
    },
    "externalIds": {
      "description": "list of external ids for the building",
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
      "description": "building code",
      "type": "string"
    },
    "description": {
      "description": "building description",
      "type": "string"
    },
    "campus": {
      "description": "building campus",
      "type": "string"
    },
    "buildingTypeRef": {
      "description": "[native reference] building type",
      "type": "string"
    }
  }
}
````