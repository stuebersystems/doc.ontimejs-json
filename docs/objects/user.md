# user


```
{
	"$schema": "http://json-schema.org/draft-04/schema#",
	"title": "ontime.js format: result",
	"description": "JSON schema for the data object user",
	"type": "object",
	"properties": {
		"profile": {
			"description": "user profile",
			"type": "string",
  		    "enum": ["student", "class", "teacher", "room", "teammaster", "staff", "master", "guest"]
		},
		"homeID": {
			"description": "[native reference] teacher/student/class/room",
			"type": "string",
		},
		"homeType": {
			"description": "type of user",
			"type": "string",
  		    "enum": ["student", "class", "teacher", "room"]
		},
		"policy": {
			"description": "DAVINCI user policy",
		"type": "integer"
	    },	
		"logbutton": {
			"description": "DAVINCI  log buttion poöicy",
		"type": "integer"
	    },	

	}
}

```

