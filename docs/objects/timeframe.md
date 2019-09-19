# timeframe

Represents a timeframe. A timeframe defines the time slots at every day where lessons can be scheduled. Basically at schools a schedule has a main timeframe (the first timeframe) for lessons and a special timeframe for supervisions. If no timeframe is assigned to a class/teacher/room it is the main timeframe by default. Addiditonally every class/teacher/room can have its own timeframe.

> #### info::Note
>
> In OnTime.JS every lesson or event is scheduled by time stamps that do not necessarily fit to a time slot exactly.

```` json
{
  "$schema": "http://json-schema.org/draft-04/schema#",
  "title": "ontime.js format: timeframe",
  "description": "JSON schema for the data object timeframe",
  "type": "object",
  "properties": {
    "id": {
      "description": "native id of the timeframe",
      "type": "string"
    },
    "externalIds": {
      "description": "list of external ids for the timeframe",
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
      "description": "timeframe code",
      "type": "string"
    },
    "description": {
      "description": "timeframe description",
      "type": "string"
    },
    "timeslots": {
      "description": "list of timeslots",
      "type": "array",
      "items": [
        {
          "type": "object",
          "properties": {
            "label": {
              "type": "string"
            },
            "color": {
              "type": "integer"
            },
            "startTime": {
              "type": "string"
            },
            "finishTime": {
              "type": "string"
            }
          }
        }
      ]
    },
    "timeslotFragmentation": {
      "description": "number of sub segments per timeslot",
      "type": "integer",
      "default": 1
    }
  }
}
````