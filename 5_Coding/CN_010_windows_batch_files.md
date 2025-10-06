---
Established: 2025-01-24
Last Updated: 2025-01-24
Description: A backup of batch codes
tags:
  - batch
---
# Sources
- Internet and myself
- They were used to organize my files but eventually failed.

```batch title="openfolder"
@ECHO OFF
%SystemRoot%\explorer.exe %cd%
```



```Batch title="Create symbolic link"
@ECHO OFF
SET src=D:\Programs\MED-PC\
CD %src%

SET dst01=D:\Work\OIST\NRU\Behavioral Exps\FP-PCA\
SET dst02=D:\Work\OIST\NRU\Behavioral Exps\FP-PCA-OPG\

IF EXIST "%dst01%MED-PC Manuals" (
    ECHO Sub folder found. Deleting . . . 
    RD /S /Q "%dst01%MED-PC Manuals"
    CALL MKLINK /D "%dst01%MED-PC Manuals" "%src%Manuals"
) ELSE (
    ECHO Sub folder not found. Creating . . .
    CALL MKLINK /D "%dst01%MED-PC Manuals" "%src%Manuals"
)

IF EXIST "%dst02%MED-PC Manuals" (
    ECHO Sub folder found. Deleting . . . 
    RD /S /Q "%dst02%MED-PC Manuals"
    CALL MKLINK /D "%dst02%MED-PC Manuals" "%src%Manuals"
) ELSE (
    ECHO Sub folder not found. Creating . . .
    CALL MKLINK /D "%dst02%MED-PC Manuals" "%src%Manuals"
)

PAUSE
```

> [!caution]
> When assign variables do not add any space
> Use double quotation marks to make spaces in a directory not to break itself