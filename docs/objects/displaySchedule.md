# displaySchedule

Represents a schedule with simple time information (as opposed to a schedule with time information formulated as complex time expressions including reoccurrences etc.). A display schedule includes lesson times, supervision times, exam sitting times and/or event times. Each time entry defines the scheduled data like date, start time and end time. If one or more changes happened to this entry these information are also delivered as list of changes. If you want to display a real up-to-date timetable you must take both data into account: Schedule data and changes to the scheduled data.

```` 
{
	"$schema": "http://json-schema.org/draft-04/schema#",
	"title": "ontime.js format: displaySchedule",
	"description": "JSON schema for the data object displaySchedule",
	"type": "object",
	"properties": {
		"id": {
			"description": "native id of the display schedule",
			"type": "string"
		},
		"externalIds": {
			"description": "list of external ids for the display schedule",
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
		"scheduleRef": {
			"description": "[native reference] schedule",
			"type": "string"
		},
		"scheduleCode": {
			"description": "unique code of the schedule",
			"type": "string"
		},
		"scheduleDescription": {
			"description": "description of the schedule",
			"type": "string"
		},
		"session": {
			"description": "session of the display-schedule",
			"type": "object",
			"properties": {
				"startDate": {
					"description": "session start date",
					"type": "string"
				},
				"endDate": {
					"description": "session end date",
					"type": "string"
				}
			},
			"required": ["startDate",
			"endDate"]
		},
		"effectivity": {
			"description": "effectivity of the display-schedule",
			"type": "object",
			"properties": {
				"startDate": {
					"description": "effectivity start date",
					"type": "string"
				},
				"endDate": {
					"description": "effectivity end date",
					"type": "string"
				}
			},
			"required": ["startDate",
			"endDate"]
		},
		"weekspan": {
			"description": "start and end of the week",
			"type": "object",
			"properties": {
				"startDay": {
					"description": "start day of the week",
					"enum": ["Mon",
					"Tue",
					"Wed",
					"Thu",
					"Fri",
					"Sat",
					"Sun"]
				},
				"endDay": {
					"description": "end day of the week",
					"enum": ["Mon",
					"Tue",
					"Wed",
					"Thu",
					"Fri",
					"Sat",
					"Sun"]
				}
			},
			"required": ["startDate",
			"endDate"]
		},
		"display": {
			"description": "display configuration",
			"type": "object",
			"properties": {
				"posLabel": {
					"description": "0 = display start/finish time only, 1 = display label only, 2 = display label and start/finish time",
					"type": "integer"
				},
				"lessonColor": {
					"description": "background: 0 = default color, 1 = subject color, 2 = class color, 3 = teacher color, 4 = room color",
					"type": "integer"
				},
				"lessonGradient": {
					"description": "background: 0 = no-gradient strip, 1 = gradient strip at left with lessonColor, 2= full background with lessonColor",
					"type": "integer"
				},
				"alwaysLessonTime": {
					"description": "TRUE = display start/finish time in every lesson, FALSE = display start/finish time only in lessons that do not exactly fit to time slot",
					"type": "boolean"
				},
				"absenceReasons": {
					"description": "TRUE = show absenceResons, otherwise show no absence information",
					"type": "boolean"
				},
				"absReasonCaption": {
					"description": "TRUE = show absenceReason in caption always",
					"type": "boolean"
				}
			},
			"required": ["posLabel",
			"lessonColor",
			"lessonGradient",
			"alwaysLessonTime",
			"absenceReasons",
			"absReasonCaption"]
		},
		"lessonTimes": {
			"description": "list of all lesson times within in the display-schedule",
			"type": "array",
			"items": {
				"type": "object",
				"properties": {
					"courseType": {
						"description": "type of lesson",
						"type": "integer"
					},
					"courseRef": {
						"description": "[native reference] lesson",
						"type": "string"
					},
					"courseTitle": {
						"description": "course title, in case of changes see lessonTitle",
						"type": "string"
					},
					"courseDescription": {
						"description": "course description",
						"type": "string"
					},
					"lessonRef": {
						"description": "[native reference] lesson",
						"type": "string"
					},
					"lessonBlock": {
						"description": "lesson block",
						"type": "string"
					},
					"dates": {
						"description": "list of date values",
						"type": "array",
						"items": {
							"type": "string"
						}
					},
					"weekday": {
						"description": "weekday",
						"enum": ["Mon",
						"Tue",
						"Wed",
						"Thu",
						"Fri",
						"Sat",
						"Sun"]
					},
					"startTime": {
						"description": "start time",
						"type": "string"
					},
					"endTime": {
						"description": "end time",
						"type": "string"
					},
					"subjectCode": {
						"description": "[code reference] subject",
						"type": "string"
					},
					"studentRefs": {
						"description": "[native reference list] list of students",
						"type": "array",
						"items": {
							"type": "string"
						}
					},
					"classCodes": {
						"description": "[code reference list] list of classes",
						"type": "array",
						"items": {
							"type": "string"
						}
					},
					"teacherCodes": {
						"description": "[code reference list] list of teachers",
						"type": "array",
						"items": {
							"type": "string"
						}
					},
					"roomCodes": {
						"description": "[code reference list] list of rooms",
						"type": "array",
						"items": {
							"type": "string"
						}
					},
					"resourceCodes": {
						"description": "[code reference list] list of resources",
						"type": "array",
						"items": {
							"type": "string"
						}
					},
					"exam": {
						"description": "exam details",
						"type": "object",
						"properties": {
							"eventCategory": {
								"description": "0=exam 1=supbervision 3=assistance",
								"type": "integer"
							},
							"examNo": {
								"description": "exam no",
								"type": "string"
							},
							"chairRef": {
								"description": "[native reference] chairman of exam",
								"type": "string"
							},
							"recorder1Ref": {
								"description": "[native reference] recorder #1",
								"type": "string"
							},
							"recorder2Ref": {
								"description": "[native reference] recorder #2",
								"type": "string"
							},
							"subjectPriority": {
								"description": "priority of subject",
								"type": "string"
							},
							"examCategory": {
								"description": "category of exam",
								"type": "string"
							},
							"examGroup": {
								"description": "group id for a group of students",
								"type": "string"
							},
						},
						"required": ["eventCategory"]
					},
					
					"changes": {
						"description": "changes from the original schedule",
						"type": "object",
						"properties": {
							"caption": {
								"description": "caption for changed lesson",
								"type": "string"
							},
							"lessonTitle": {
								"description": "if newSubjectCode new lesson title instead of courseTitle",
								"type": "string"
							},
							"changeType": {
								"description": "type of change",
								"enum": ["substitution",
								"roomSubstitution",
								"assignment",
								"additionalLesson",
								"message"]
							},
							"information": {
								"description": "short summary of changes",
								"type": "string"
							},
							"newSubjectCode": {
								"description": "[code reference] new subject",
								"type": "string"
							},
							"newTeacherCodes": {
								"description": "[code reference list] new list of teacher",
								"type": "array",
								"items": {
									"type": "string"
								}
							},
							"newRoomCodes": {
								"description": "[code reference list] new list of rooms",
								"type": "array",
								"items": {
									"type": "string"
								}
							},
							"newClassCodes": {
								"description": "[code reference list] new list of classes",
								"type": "array",
								"items": {
									"type": "string"
								}
							},
							"newResourceCodes": {
								"description": "[code reference list] new list of resources",
								"type": "array",
								"items": {
									"type": "string"
								}
							},
							"absentTeacherCodes": {
								"description": "[code reference list] new list of teacher",
								"type": "array",
								"items": {
									"type": "string"
								}
							},
							"absentRoomCodes": {
								"description": "[code reference list] new list of rooms",
								"type": "array",
								"items": {
									"type": "string"
								}
							},
							"absentClassCodes": {
								"description": "[code reference list] new list of classes",
								"type": "array",
								"items": {
									"type": "string"
								}
							},
							"reasonType": {
								"description": "type of absence",
								"enum": ["teacherAbsence",
								"classAbsence",
								"roomAbsence"]
							},
							"reasonCode": {
								"description": "[code reference] absence reason for teacher, class or room",
								"type": "string"
							},
							"cancelled": {
								"description": "TRUE, if lesson was cancelled and not substituted",
								"type": "boolean"
							},
							"cancelReason": {
								"description": "[native reference] to lesson cancel reason",
								"type": "string"
							},
							"information": {
								"description": "information text",
								"type": "string"
							},
							"message": {
								"description": "message text",
								"type": "string"
							},
							"modified": {
								"description": "date time stamp of last change",
								"type": "string"
							}
						}
					}
				}
			}
			"required": ["date",
			"weekday",
			"startTime",
			"endTime",
			"subjectCode"]
		}		

		"supervisionTimes": {
			"type": "array",
			"items": {
				"type": "object",
				"properties": {
					"supervisionRef": {
						"description": "[native reference] supervision",
						"type": "string"
					},
					"supervisionTitle": {
						"description": "supervision title",
						"type": "string"
					},
					"date": {
						"description": "date of the supervision instance",
						"type": "string"
					},
					"weekday": {
						"description": "weekday of the supervision instance",
						"enum": ["Mon",
						"Tue",
						"Wed",
						"Thu",
						"Fri",
						"Sat",
						"Sun"]
					},
					"startTime": {
						"description": "start time of the supervision instance",
						"type": "string"
					},
					"endTime": {
						"description": "end time of the supervision instance",
						"type": "string"
					},
					"areaCode": {
						"description": "unique area code",
						"type": "string"
					},
					"teacherCodes": {
						"description": "list of assigned unique teacher codes",
						"type": "array",
						"items": {
							"type": "string"
						}
					},
					"changes": {
						"description": "list of changes from the original schedule",
						"type": "object",
						"properties": {
							"changeType": {
								"description": "type of change",
								"enum": ["substitution",
								"message"]
							},
							"information": {
								"description": "short summary of changes",
								"type": "string"
							},
							"newTeacherCodes": {
								"description": "[code reference list] new list of teacher",
								"type": "array",
								"items": {
									"type": "string"
								}
							},
							"absentTeacherCodes": {
								"description": "[code reference list] new list of teacher",
								"type": "array",
								"items": {
									"type": "string"
								}
							},
							"absenceReasonType": {
								"description": "type of absence",
								"enum": ["teacherAbsence"]
							},
							"absenceReasonCode": {
								"description": "[code reference] absence reason for teacher",
								"type": "string"
							},
							"cancelled": {
								"description": "TRUE, if supervision was cancelled and not substituted",
								"type": "boolean"
							},
							"cancelReasonCode": {
								"description": "[code reference] to supervision cancel reason",
								"type": "string"
							},
							"message": {
								"description": "message text",
								"type": "string"
							},
							"lastChange": {
								"description": "date time stamp of last change",
								"type": "string"
							}
						}
					}
				},
				"required": ["date",
				"weekday",
				"startTime",
				"endTime",
				"areaCode"]
			}
		},
		"eventTimes": {
			"type": "array",
			"items": {
				"type": "object",
				"properties": {
					"eventRef": {
						"description": "[native reference] event",
						"type": "string"
					},
					"eventCaption": {
						"description": "event caption",
						"type": "string"
					},
					"eventDescription": {
						"description": "event description",
						"type": "string"
					},
					"eventUrl": {
						"description": "link to web page with additional informations",
						"type": "string"
					},
					"eventCategoryRef": {
						"description": "[native reference] event category",
						"type": "string"
					},
					"eventStatus": {
						"description": "event status",
						"enum": ["planned",
						"confirmed",
						"cancelled"]
					},
					"eventLocation": {
						"description": "event location",
						"type": "string"
					},
					"startDate": {
						"description": "start date of the event",
						"type": "string"
					},
					"endDate": {
						"description": "end date of the event",
						"type": "string"
					},
					"startTime": {
						"description": "start time of the event",
						"type": "string"
					},
					"endTime": {
						"description": "end time of the event",
						"type": "string"
					}
				},
				"required": ["eventCaption",
				"startDate",
				"endDate",
				"startTime",
				"endTime"]
			}
		}
	}
}

````