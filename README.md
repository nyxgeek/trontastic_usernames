# Trontastic Usernames

## Overview

Username lists derived from a 3-year survey of Azure. Also, survey scripts that were used in this research.


### Files

| File | Example | Description|
| ------------- | ------------- | ------------- |
| trontastic_all.250k.txt  | info, helpdesk, jsmith, msmith, mark, etc | Top 250 all usernames in all formats  |
| trontastic_all.500k.txt  | info, helpdesk, jsmith, msmith, mark, etc | Top 500k all usernames in all formats  |
| trontastic_service_accounts.txt  | admin, info, noreply, etc | Top service accounts  |
| trontastic_john.smith_250k.txt
| trontastic_john.txt  | first names |
| trontastic_smith.txt | last names  | 
| create_usernames_from_name.sh  | jsmith, john.smith, john, smith, jjsmith, etc | Generate many possible usernames from a name  |


In addition to these lists, there are additional lists available in all popular username formats.

### Folders

| Folder | Example | Description|
| ------------- | ------------- | ------------- |
| surveys  | N/A | Survey lists in different formats  |
| census_lists  | N/A | Generator script to create census-based wordlists  |



## Sources
All username lists were publicly sourced, being derived from US Census data. The service account lists are a combination of various common account names, augmented by ChatGPT's suggestions.


## Survey Lists
The survey lists are far from perfect. My goal had originally been to scale them in size compared to the number of permutations. However, some
lists get unwieldly for a fast survey (john.jame.smith format, for instance), needing many more permutations than jsmith to find the same relative 
number of people at a hypothetical organization. Other lists got much too small if I had tried to scale them properly. Finally, names are complicated. Their popularity
is represented as a long tail graph, with the bulk of names falling within a relatively small portion of the population. The curve between first names and last names goes at different
rates and this difference was not taken into account when performing combinations of first.last. So -- what I'm saying is, it's not perfect, and maybe some real sharp maths
person can suggest a better breakdown.


## Census Lists
This folder contains a list of census-derived top first names and last names, as well as some middle initials from trontastic research. These files, coupled with a generator script, can be used to create massive username lists in all formats.


## create_usernames_from_name.sh
Will output a file containing usernames in many formats based off of a first and last name that is provided.

Example:
```
./create_usernames_from_name.sh john doe johndoe.txt
```


A simple bash script that takes a first and last name, and generates possible usernames from them.
