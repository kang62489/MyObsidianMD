---
Established: 2024-12-27
Last Updated: 2024-12-29
Description: Insert new key-value pairs to an existing json/dictionary structure
tags:
  - python
---
# Purposes
-  To calculate the weeks of ages and incubation of the animal and then add them to a existing metadata json file
## Example
```python
from collections import OrderedDict
import json

ages = [8, 18]
metadata = {
			"Animal":{
						"ID": "",
				        "Strain_Genotype": "",
				        "Species": "",
				        "Sex": "",
				        "Date of Birth": ["2024-05-31"],
				        "Injected brain area": "",
				        "Coordinates": "",
				        "Virus_L": "",
				        "Virus_R": "",
				        "Date of Injection": ["2024-07-19"]
			}
}
# insert a new term "Age" to the entered metadata file
insert_pos_age = list(metadata["Animal"]).index("Date of Birth")
items_of_animal = list(metadata["Animal"].items())
keys_of_animal = [key[0] for key in items_of_animal]

if not "Age" in keys_of_animal:
	items_of_animal.insert(insert_pos_age + 1, ("Age", [str(age)+" weeks" for age in ages]))
	metadata["Animal"] = OrderedDict(items_of_animal)
	print("Term: Age is added to the metadata")
	print(json.dumps(metadata, indent=4))
else:
	metadata["Animal"]["Age"] = [str(age)+" weeks" for age in ages]
	print("Term: Age in the metadata is updated")
	print(json.dumps(metadata, indent=4))

```

> [!info]
> 1. The code can be run in reading mode (hotkey: Alt+E)