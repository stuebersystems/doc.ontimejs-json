# Introduction

OnTime.JS is an Open Source library for displaying timetable and calendar data. As data source it uses JSON data described in this documentation. A JSON schema is a meta language for describing JSON data. The syntax of a JSON schema is JSON and can be validated. Please have a look at http://json-schema.org for more information on JSON schemata.

OnTime.JS widgets expect from data sources [onplan objects](objects/onplan.md).
OnTime.JS objects have a unique id. Also every objects can store references to other applications in externalIds. In OnTime.JS you can identify objects by it's native id or by its externalIds. With the suffix ``Ref`` or ``Refs`` (e.g. ``teamRef``) the id of an object (here object "team") is referenced. For better readability in some special cases there is the var of an object referenced e.g. in ``displaySchedule`` property ``subjectRef``. Objects like classes, teachers, rooms, subject have a code that is a short name for display. A code must be unique for that type of objects.

OnTime.JS objects are designed for efficiently transporting timetable display data to display devices like Web front ends, E-Boards (public displays), apps and digital room signs. Therefore we tried to find a compromise between versatility and processing performance. Examples for OnTime.JS driven solutions you will find here:

* [DAVINCI WEBBOX (in German)](https://davinci-webbox.stueber.de/)
* [DAVINCI WEBBOX (in English)](https://davinci-webbox.stueber.co.uk/)
