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



### Tests on first:last name counts

Here I tested different combinations of first x last names. The naming indicates (first)x(last). So, 400x25k means 400 first names, 25000 last names.
Results are only from runs where usernames were found, hence the small 'totalruns' numbers.

```
+-----------------------------------------------+-----------+------------+--------------+
| userlist                                      | totalruns | totalfound | averagefound |
+-----------------------------------------------+-----------+------------+--------------+
| USERNAMES/tron_john.smith_400x25k_v1/xaa      |        28 |      34421 |    1229.3214 |
| USERNAMES/tron_john.smith_ax500_v1/xaa        |      1319 |    1558141 |    1181.3048 |
| USERNAMES/tron_john.smith_500x20k_v1/xaa      |      1351 |    1500346 |    1110.5448 |
| USERNAMES/tron_john.smith_250x40k_v1/xaa      |        34 |      30847 |     907.2647 |
| USERNAMES/tron_john.smith_150x66k_v1/xaa      |        11 |       8383 |     762.0909 |
| USERNAMES/tron_john.smith_200x50k_v1/xaa      |       166 |      46700 |     281.3253 |
| USERNAMES/tron_john.smith_1kx10k_v1/xaa       |      5646 |    1509946 |     267.4364 |
| USERNAMES/tron_john.smith_100x100k_v1/xaa     |       193 |      39033 |     202.2435 |
```

For jsmith, I approached testing in a more structured manner. Taking the jsmith benchmark results, I took the top results, and tested various jsmith combinations against the top 67 of these. This number is arbitrary and was based on when I decided to pause them all.

Similar to the john.smith listing, the jsmith listing variations are denoted by (first initial)x(last). So 17x2941 means 17 most common first initials and 2941 most common last names.

The list of first initials used was derived from the complete trontastic username list.

```
3509657 j
3503166 a
3243364 m
2951495 s
2474269 c
1953051 d
1870843 k
1838726 r
1553709 l
1553461 b
1536929 t
1203876 e
 980266 p
 922442 n
 897996 g
 840309 h
 712378 i
 516009 w
 486357 f
 472081 v
 283707 o
 224011 y
 194617 z
  53819 q
  43247 x
  41594 u
```


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
