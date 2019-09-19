# note

This is a note (alarm) message for all DAVINCI room signs within the domain. It switches room signs into special alert mode. This alert mode should be stopped by a "state=whiteout" message.

```
	{
		"$schema": "http://json-schema.org/draft-04/schema#",
		"title": "ontime.js format: alarm",
		"description": "JSON schema for the data object alarm",
		"type": "object",
		"properties": {
			"state": {
				"description": "state code",
				"type": "string"
			},
			"msg": {
				"description": "message text to be displayed",
				"type": "string"
			},
		}
	}

```

