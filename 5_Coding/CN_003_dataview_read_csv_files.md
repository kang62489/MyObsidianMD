---
Established: 2024-12-27
Last Updated: 2024-12-29
Description: Read multiple metadata stored in CSV files by dataview
tags:
  - dataview
  - obsidian
---
# Purposes
- To rapidly filter out the imaging files which fit certain conditions of analysis by dataview
## Example
### CSV files
- Two csv files were put in the subfolder "csv files for testing"

### Dataview codes
```dataview
TABLE WITHOUT ID Filename, Timestamp, OBJ, Signal, Exposure, Light, Intensity, row["Slice_#"] as "Slice_#", row["Cell/Pos"] as "Cell/Pos", Puff, row["P.Conc"] as "Puff Concentration", row["P.Period"] as "Puff Period", row["P.Pressure"] as "Puff Pressure"
FROM csv("5_Coding/csv files for testing/20240823_REC summary_updated.csv") or csv("5_Coding/csv files for testing/20241219_REC summary_updated.csv")
WHERE signal="GFP" and Light="LED" and Puff="J60" and row["P.Period"]="50ms"
```


> [!info]
> 1. Use only "row" function, square brackets, and double quotation marks to specify the columns whose names contains special characters.
> 2. Files in the same vault can be referred easily by the form of path below
> 	- "root folder name/subfolder/filename.extension"
