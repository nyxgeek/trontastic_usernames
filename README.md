# Trontastic Usernames

## Overview

Username lists derived from a 3-year survey of Azure. Also, survey scripts that were used in this research.
- Total of 70m usernames collected
- 3.6m+ unique john.smith format
- All lists were filtered with US Census lists - only names already in public data are included


### Files

| File |  Description |
| ------------- | ------------- |
| trontastic_all.250k.txt   | Top 250 all usernames in all formats  |
| trontastic_service_accounts.txt | Top service accounts  |
| trontastic_john.smith_250k.txt | Top 250k john.smith formatted names |
| trontastic_john.txt  | first names |
| trontastic_smith.txt | last names  | 
| create_usernames_single.sh  | Generate many possible usernames from a single full name  |
| create_usernames_lists.sh | Generate username lists in 17 common formats based off a list of first and last names|

In addition to these lists, there are additional lists available in all popular username formats.

### Folders

| Folder | Description|
| ------------- | ------------- |
| surveys  | Survey lists in different formats  |
| census_lists | Generator script to create census-based wordlists  |
| counts | Lists with user counts | 



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


## create_usernames_single.sh
Will output a file containing usernames in many formats based off of a first and last name that is provided.

Example:
```
./create_usernames_single.sh john doe johndoe.txt
```

## create_usernames_lists.sh
Will output a file containing usernames in many formats based off of a first and last name file that is provided. ** Warning ** This can take up like 5GB+ of space.

Example:
```
./create_usernames_lists.sh firstnames.txt lastnames.txt
```


A simple bash script that takes a first and last name, and generates possible usernames from them.
