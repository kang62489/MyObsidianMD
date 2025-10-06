# Lab Presentations
```dataview
TABLE WITHOUT ID file.link as Filename, Descriptions as "Descriptions", last-updated as "Last Updated"
FROM "3_Meeting"
WHERE contains(file.name, "Mtg_LAB")
SORT file.link DESC
```

# Weekly Discussion with Jeff
```dataview
TABLE WITHOUT ID file.link as Filename, Descriptions as "Descriptions", last-updated as "Last Updated"
FROM "3_Meeting"
WHERE contains(file.name, "Mtg_WD")
SORT file.line DESC
```

# Discussion with collaborators
```dataview
TABLE WITHOUT ID file.link as Filename, Descriptions as "Descriptions", last-updated as "Last Updated"
FROM "3_Meeting"
WHERE contains(file.name, "Mtg_CR")
SORT file.link DESC
```
