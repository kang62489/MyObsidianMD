---
Established: 2024-12-27
Last Updated: 2025-03-08
Description: List the notes which cite a certain reference by dataview inline field annotations
tags:
  - dataview
  - obsidian
---
# Purposes
- To quickly find in which notes a certain reference is cited
- To test inline metadata annotation of dataview
## Example_1
### A list item
- This paragraph is related to the cited paper. (Ref::Author_Publicated-In)

### Dataview codes
```dataview
TABLE WITHOUT ID file.folder as Folder, file.link as Title, replace(replace(L,"(Ref::Author_Publicated-In)",""),"[Ref::Author_Publicated-In]","") as List-Items
FLATTEN file.lists.text as L
WHERE contains(L,"Author_Publicated-In")
```
> [!caution]
> - For showing the contexts, the inline field annotation must be used in the list items.


> [!info]
> 1. Different form of inline field annotations
> 	- [Ref::Author_Publicated-In] (Show highlighted and Bold field name)
> 	- (Ref::Author_Publicated-In) (Hidden field name)
> 2. Use "replace" function to hide tags or inline field annotations


## Example_2
### Another way to list the position of reference
```dataview
TABLE WITHOUT ID file.folder as "Folder", file.link as "Title", split(crossRef, ", ")[length(split(crossRef, ", "))-1] as "Note_Location", split(crossRef, ", ")[0] as "Source_Location"
FLATTEN crossRef
WHERE contains(crossRef,"Purves") OR contains(crossRef, "Neuroscience_6ed")
```

> [!info]
> Since this method is not item-list, therefore it cannot show the content before.

> [!caution]
> Use "FLATTEN" to list different values of metadata from the same field name.
