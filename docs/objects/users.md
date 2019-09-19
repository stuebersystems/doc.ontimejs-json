# users

```
{
	"$schema": "http://json-schema.org/draft-04/schema#",
	"title": "ontime.js format: result",
	"description": "JSON schema for the data object users",
	"properties": {	
		"users": {
			"description": "[native reference list] list of students",
			"type": "array",
			"items": {
				"profile": {
					"description": "user profile",
					"type": "string",
					"enum": ["student",
					"class",
					"teacher",
					"room",
					"teammaster",
					"staff",
					"master",
					"guest"]
				},
				"homeID": {
					"description": "[native reference] teacher/student/class/room",
					"type": "string",
					
				},
				"homeType": {
					"description": "type of user",
					"type": "string",
					"enum": ["student",
					"class",
					"teacher",
					"room"]
				}
		
			}
		},
	}
}
```

