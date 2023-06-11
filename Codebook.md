# A cleaned version of UN General Assembly (UNGA) vote data

check original data and codebook from:\
    &emsp; https://dataverse.harvard.edu/dataset.xhtml?persistentId=hdl:1902.1/12379

**Data range: 1991-2021**

### List of all column names:

```
'date' 'year' 'rcid' 'resid' 'session'
'ccode' 'Country' 'Countryname' 'CountrynameCOW' 'vote'
'unres' 'yes' 'no' 'abstain' 'amend' 'para' 'importantvote'
'me' 'nu' 'di' 'hr' 'co' 'ec'
```

### Details:

`date` - date of vote

`year` - year of vote, derived from `date`, NOT using original dataset `year` column

`rcid` - roll call vote id (RCID)

`resid` - new roll call vote id, number is sequential within sessions (`session` + 3 digit sequential numve)

`session` - UN Session (1-73)\
&emsp;*Note that sessions typically run from September-December but there are typically some votes that take place in the following year*

`ccode` - COW country code

`Country` - three letter abbreviation of country names, provided by COW, NOT using original dataset `Country` column

`Countryname` - country names in the original dataset, not unique for each country

`CountrynameCOW` - country names provided by COW, unique for each country

`vote` - vote choice of each country at each vote

    1 – Yes
    2 – Abstain
    3 – No
    8 – Absent
    9 – Not a member

`unres` - UN Resolution number

`yes`, `no`, and `abstain` - total number of Yes, No, and Abstain in each vote (vote result)

`amend` - whether the vote was on an amendment

`para` - whether the vote was on a paragraph rather than an entire resolution

`importantvote` - vote identified as important by U.S. State Department report Voting Practices in the United Nations.\
&emsp;*NOTE: not available for all years*

#### Issue codes:

These are based on searches in descriptions. They have been subjected to a rudimentary visual check but they may not be 100% accurate

`me`: Votes relating to the Palestinian conflict\
`nu`: Votes relating to nuclear weapons and nuclear material\
`di`: Votes relating to arms control and disarmament\
`hr`: Votes relating to human rights\
`co`: Votes relating to colonialism\
`ec`: Votes relating to (economic) development
