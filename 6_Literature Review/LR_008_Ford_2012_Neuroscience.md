# Log
## 2025-Mar-13
- Check the receptors on DA terminals
	- I want to use the enhancer-AAV toolbox to express DA sensors (DLight, RDLight) specifically on DA terminals in striatum by RO injection. The enhancer is the DNA fragment specific to certain types of neurons, therefore I was looking for the receptors on DA neurons.


# Cited
```dataview
TABLE WITHOUT ID file.folder as "Folder", file.link as "Title", split(crossRef, ", ")[length(split(crossRef, ", "))-1] as "Note_Location", split(crossRef, ", ")[0] as "Source_Location"
FLATTEN crossRef
WHERE contains(crossRef,"Ford") AND contains(crossRef, "2012_Neuroscience")
```
