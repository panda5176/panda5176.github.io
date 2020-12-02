---
layout: post
title: Maltorean
category: Repositories
---

# MalToReAn   
### MALDI-TOF Result Analyzer by physcopatens12   

Maltorean is desinged to analyze MALDI-TOF result file from SNU Proteomics Core Facility.   
   
Peptide read counts are converted into bar graph, indexed and aligned with reference protein.   
   
Please read README.md or [https://github.com/physcopatens12/maltorean](https://github.com/physcopatens12/maltorean).   

---------------------------------------------------------------------

**REQUIRED LIBRARY:**   
```
Pandas & Matplotlib   
```

**USAGE:**   
```
$ python3 maltorean.py [-h] -M META [-R READ] [-W WRITE]
```   

**OPTIONAL ARGUMENTS:**   
```
-h, --help   
: show this help message and exit   
-M META, --meta META   
: .csv file including metadata   
-R READ, --read READ   
: folder path of read MALDI-TOF .csv files   
-W WRITE, --write WRITE   
: folder path to write files   
```

**INPUT FORMAT:**   
```
Reads metadata sheet .csv file into pandas dataframe.   
File must be constructed with columns (without header and index):   
>1) *MALDI-TOF result file name (without .csv),   
>2) Target reference protein name (same in result file),   
>3) Amino acid sequence of reference protein.   

>*MALDI-TOF result .csv file is from Unipeptide sheet of .xlsx file.   
>Columns are Protein name, Types of peptide (count) and Sum of peptide spectrum.   
```

**OUTPUT FORMAT:**   
```
Writes a .csv sheet of reference protein amino acid and its frequency.   
   
Draws bar plot of amino acid frequency indexed by reference protein sequence.   
Output size is 2000px X 5 px and formats are .pdf and .png.   
```
