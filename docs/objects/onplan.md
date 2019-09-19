# onplan




```
{
	"$schema": "http://json-schema.org/draft-04/schema#",
	"title": "ontime.js format: onplan",
	"description": "JSON schema for the data object onplan",
	"type": "object",
	"properties": {
		"about"		: { "$ref": "#about" },
		"alarm"		: { "$ref": "#note" },
		"result" 	: { "$ref": "#result" },
		},
		"user": {
			"type": "object",
			"oneOf": [
				{ "$ref": "#user" },
				{ "$ref": "#users" }
			]
		}
	}
}

```

