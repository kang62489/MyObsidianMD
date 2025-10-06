---
Established: 2024-01-21
Last Updated: 2024-01-21
Description: A memo of operations of pandas dataFrame
tags:
  - python
  - pandas
---
# Sources
> [!cite]
> Collect from the experiences of making my python GUI - "Metadata Generator"
> 

```python title="dataFrame Operations"
import pandas as pd
import json
import random
from tabulate import tabulate

rowNames = [
    "OBJ",
    "EXC",
    "LEVEL",
    "EMI",
    "SLICE",
    "SAMPLE",
    "FRAMES",
    "FPS",
    "CAM.TRIG.MODE"
]

columnNames = ["VALUE"]

values = []

OBJ = ["10X", "60X"]
EXC = ["HLG", "LED"]
EMI = ["IR", "GREEN", "RED"]

dummies = 3
dfs = {}
for i in range(dummies):
    values = [""] * len(rowNames)
    values[0] = random.choice(OBJ)
    values[1] = random.choice(EXC)
    values[3] = random.choice(EMI)
    
    df = pd.DataFrame({columnNames[0]: values}, index=rowNames)
    dfs[f"Sheet_{i}"] = df.to_dict(orient='dict')
     

# Save the dictionary to a JSON file
with open('models/tagSet_default.json', 'w') as f:
    json.dump(dfs, f, indent=4)
    
    
with open('models/tagSet_default.json', 'r') as f:
    data = json.load(f)
    df1 = pd.DataFrame.from_dict(data['Sheet_1'])
    print(tabulate(df1, headers='keys', tablefmt='pretty'))
    df2 = pd.DataFrame.from_dict(data['Sheet_2'])
    print(tabulate(df2, headers='keys', tablefmt='pretty'))
```

> [!info] 


> [!seealso]

