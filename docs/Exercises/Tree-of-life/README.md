# The Tree of Life dataset
Final exercise on data wrangling with tidyverse

A real study case from Mammola et al., 2023 (https://doi.org/10.7554/eLife.88251.3)

Authors: Matteo Chialva & Martino Adamo


> [!NOTE]
> - use tidyverse functions (and pipe them where possible!)
> - load your final *.R script file in the Moodle page of the course[^1].

[^1]: If you do not have access to the Moodle platform yet, please e-mail us your results!

# Task 1 - import data
- Import the Tree of Life Dataset SampleTREE_TraitCompiled.csv) from the Dataset folder [here](https://raw.githubusercontent.com/mchialva/PhDToolbox2026/main/docs/Exercises/Tree-of-life/SampleTREE_TraitCompiled.csv) into the *ToL* object

> [!IMPORTANT]
> + If you use read.table() function please add the following arguments to avoid importing issues:
> + Please, check the field separator before importing the file. File extension is .csv, but the separator could not be the comma.

```
read.delim(..., quote="\"", fill=T)
```
- Check the object class, structure and dimensions of the imported object

# Task 2 - Adjust columns and their content
- remove *Notes* and *fossil_status* columns

- set *name* columns as rownames

- remove parenthes from *author* column and store the results into a new column called *author_clean*

- Add the a new column with the full name of *IUCN* columns by using th IUCN categories dataset in the Dataset folder

> [!CAUTION]
> the IUCN categories dataset contains redundant information, you need to parse the table before using it.

# Task 3 - Summarize data

- Which is the mean wikipedia mean month page wiews and total WoS citations (*Total_wos* column) of the different kingdoms?

- Which are the most cited species for each group?

> [!TIP]
> You can achieve these goals by using the functions we mentioned during the course lessons.
> However, the **top_n()** function can make the job easier. Possibly, explore both the ways.

