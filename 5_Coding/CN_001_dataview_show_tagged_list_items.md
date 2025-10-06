---
Established: 2024-12-27
Last Updated: 2024-12-29
Description: Show list items containing a certain tag in dataview
tags:
  - dataview
  - obsidian
---
# Purposes
- To list the contexts of items with a certain tag
- The original purpose was to list different status of tasks such as "completed", "failed", "postponed". 
## Example
### An ordered and unordered lists
- AAA
	- A1 
	- A2 #example_tag01 
- BBB
	- B1
	- B2
	- B3 #example_tag01
- CCC
	- C3 #example_tag01


1. Goal 1
	1. sub-task 1
	2. sub-task 2 (not showing "Goal 1" in the dataview) #example_tag01
	3. sub-task 3
2. Goal 2
	2.1 sub-task 1 (showing "Goal 2" in the dataview) #example_tag01 
### Dataview codes
```dataview
LIST without id replace(L.text,"#example_tag01","")
From "5_Coding/CN_001_dataview_show_tagged_list_items"
FLATTEN file.lists as L
WHERE contains(L.tags, "#example_tag01")
```
> [!caution]
A different effect for customized ordered list items
