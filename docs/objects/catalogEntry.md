# catalogEntry

Represents a catalogue entry.

```` json
{
  "$schema": "http://json-schema.org/draft-04/schema#",
  "title": "ontime.js format: catalogEntry",
  "description": "JSON schema for the data object catalogEntry",
  "type": "object",
  "properties": {
    "id": {
      "description": "native id of the catalog entry",
      "type": "string"
    },
    "externalIds": {
      "description": "list of external ids for the catalog entry",
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
      "description": "catalog entry code",
      "type": "string"
    },
    "statisticalCode": {
      "description": "code for statistical analysis",
      "type": "string"
    },
    "description": {
      "description": "catalog entry description",
      "type": "string"
    }
  }
}
````