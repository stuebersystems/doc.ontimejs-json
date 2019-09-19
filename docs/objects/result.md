# result


```
{
	"$schema": "http://json-schema.org/draft-04/schema#",
	"title": "ontime.js format: result",
	"description": "JSON schema for the data object result",
	"type": "object",
	"properties": {
		"areas": {
			"description": "list of areas",
			"type": "array",
			"items": { "$ref": "#areas" }
		},
		"teacherAbsenceReasons": {
			"description": "list of teacher absence reasons",
			"type": "array",
			"items": { "$ref": "#teacherAbsenceReason" }
		},
		"classAbsenceReasons": {
			"description": "list of class absence reasons",
			"type": "array",
			"items": { "$ref": "#classAbsenceReason" }
		},
		"roomAbsenceReasons": {
			"description": "list of room absence reasons",
			"type": "array",
			"items": { "$ref": "#roomAbsenceReason" }
		},
		"buildings": {
			"description": "list of buildings",
			"type": "array",
			"items": { "$ref": "#buildings" }
		},
		"classes": {
			"description": "list of classes",
			"type": "array",
			"items": { "$ref": "#class" }
		},
		"courses": {
			"description": "list of courses",
			"type": "array",
			"items": { "$ref": "#teacher" }
		},
		"resources": {
			"description": "list of resources",
			"type": "array",
			"items": { "$ref": "#resources" }
		},
		"rooms": {
			"description": "list of rooms",
			"type": "array",
			"items": { "$ref": "#rooms" }
		},
		"students": {
			"description": "list of students",
			"type": "array",
			"items": { "$ref": "#students" }
		},
		"teams": {
			"description": "list of teams",
			"type": "array",
			"items": { "$ref": "#teams" }
		},
		"calCategories": {
			"description": "list of calendar categories",
			"type": "array",
			"items": { "$ref": "#calCategory" }
		},
		"roomstatus": {
			"description": "list of roomstatus",
			"type": "array",
			"items": { "$ref": "#roomstatus" }
		},
		"subjects": {
			"description": "list of subjects",
			"type": "array",
			"items": { "$ref": "#subject" }
		}
	}
}

```

