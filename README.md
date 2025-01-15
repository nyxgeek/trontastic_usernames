# Trontastic Usernames

## Overview

These are top username lists in different formats, as well as survey lists and service account lists that were used as part of Azure Survey 2025.

### Files

| File | Example | Description|
| ------------- | ------------- | ------------- |
| trontastic_all.100k.txt  | info, helpdesk, jsmith, msmith, mark, etc | Top 100k all usernames in all formats  |
| trontastic_all.500k.txt  | info, helpdesk, jsmith, msmith, mark, etc | Top 500k all usernames in all formats  |
| trontastic_users.100k.txt  | jsmith, mark, john.doe, etc | Top 100k all usernames - No service accounts  |
| trontastic_users.500k.txt  | jsmith, mark, john.doe, etc | Top 500k all username - No service accounts  |
| service_accounts.txt  | admin, info, noreply, etc | Top service accounts  |
| top_6digit.100k.txt  | 123456 | Top 6 digit numeric username ranges  |
| top_7digit.100k.txt  | 1234567 | Top 7 digit numeric username ranges  |
| create_usernames.sh  | jsmith, john.smith, john, smith, jjsmith, etc | Generate usernames from a name  |


In addition to these lists, there are additional lists available in all popular username formats.

### Folders

| Folder | Example | Description|
| ------------- | ------------- | ------------- |
| surveys  | N/A | Survey lists in different formats  |
| by_format  | N/A | Top lists in various username formats  |
| census_lists  | N/A | Generator script to create census-based wordlists  |
| derived_lists  | N/A | Generator script to create trontastic-based wordlists |



## Sources
All username lists were publicly sourced, being derived from US Census data. The service account lists are a combination of various common account names, augmented by ChatGPT's suggestions.


## Survey Lists
The survey lists are far from perfect. My goal had originally been to scale them in size compared to the number of permutations. However, some
lists get unwieldly for a fast survey (john.jame.smith format, for instance), needing many more permutations than jsmith to find the same relative 
number of people at a hypothetical organization. Other lists got much too small if I had tried to scale them properly. Finally, names are complicated. Their popularity
is represented as a long tail graph, with the bulk of names falling within a relatively small portion of the population. The curve between first names and last names goes at different
rates and this difference was not taken into account when performing combinations of first.last. So -- what I'm saying is, it's not perfect, and maybe some real sharp maths
person can suggest a better breakdown.


## By-Format Lists
The ```by_format``` folder contains top username lists in various formats based on delimiters. These are:
- name (john, smith, jsmith, smithj, johnsmith, smithjohn etc)
- name.name (john.smith, smith.john)
- j.smith (j.smith, s.john)
- smith.j (smith.j, john.s)
- john.j.smith
- john.james.smith

## Census Lists
This folder contains a list of census-derived top first names and last names, as well as some middle initials from trontastic research. These files, coupled with a generator script, can be used to create massive username lists in all formats.

## Derived Lists
This folder contains a list of trontastic-derived top first names and last names, as well as popular middle initials. These files, coupled with a generator script, can be used to create massive username lists in all formats.



## create_usernames.sh

```
./create_usernames.sh john doe johndoe.txt
```

A simple bash script that takes a first and last name, and generates possible usernames from them.
