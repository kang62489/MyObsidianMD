# Cited
```dataview
TABLE WITHOUT ID file.folder as "Folder", file.link as "Title", split(crossRef, ", ")[length(split(crossRef, ", "))-1] as "Note_Location", split(crossRef, ", ")[0] as "Source_Location"
FLATTEN crossRef
WHERE contains(crossRef,"Purves") AND contains(crossRef, "Neuroscience_6ed")
```
