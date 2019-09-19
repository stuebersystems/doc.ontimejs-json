# resource

Represents a resource, e.g. beamer, audio device, toolbox.

```` json
{
  "$schema": "http://json-schema.org/draft-04/schema#",
  "title": "ontime.js format: resource",
  "description": "JSON schema for the data object resource",
  "type": "object",
  "properties": {
    "id": {
      "description": "native id of the resource",
      "type": "string"
    },
    "externalIds": {
      "description": "list of external ids for the resource",
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
      "description": "resource code",
      "type": "string"
    },
    "description": {
      "description": "resource description",
      "type": "string"
    },
    "color": {
      "description": "resource color",
      "type": "integer"
    },
    "resourceTypeRef": {
      "description": "[native reference] resource type",
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