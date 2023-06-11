# A cleaned version of UN General Assembly vote data

check original data and codebook from:
    https://dataverse.harvard.edu/dataset.xhtml?persistentId=hdl:1902.1/12379

**Data range: 1991-2021**

List of all column names:

'date' 'year' 'rcid' 'resid' 'session'\
'ccode' 'Country' 'Countryname' 'CountrynameCOW' 'vote'\
'unres' 'yes' 'no' 'abstain' 'amend' 'para' 'importantvote'\
'me' 'nu' 'di' 'hr' 'co' 'ec'


Variables raw UNGA dataset
rcid – roll call vote id RCID, can be matched with ICPSR id until 1985. Ids>9000 are the emergency special sessions not in the original ICPSR dataset. 

Resid – New roll-call vote id, number is sequential within sessions (session + 3 digit sequential numve)
 
ccode- COW country code

member- Is country a member of the United Nations?

vote – Vote choice
1 – Yes
2 – Abstain
3 – No
8 – Absent
9 – Not a member

Country- three letter abbreviation, country name

Countryname – UNGA session 

year- year of vote

session- UN Session (1-73): Note that sessions typically run from September-December but there are typically some votes that take place in the following year. 
date – date of vote

unres – UN Resolution number. This does not always correspond to the actual UN resolution number before 1985 due to inconsistencies in the original ICPSR data.

amend-  whether the vote was on an amendment 
para- whether the vote was on a paragraph rather than an entire resolution 
short- short description
descr – longer description
important- Vote identified as important by U.S. State Department report Voting Practices in the United Nations. NOTE: not available for all years!!!!!
Issue codes: These are based on searches in descriptions. They have been subjected to a rudimentary visual check but they may not be 100% accurate,
ME: Votes relating to the Palestinian conflict (19%)
NU: Votes relating to nuclear weapons and nuclear material (13%)
DI: Votes relating to arms control and disarmament (16%)
CO: Votes relating to colonialism (18%)
HR: Votes relating to human rights (17%)
EC: Votes relating to (economic) development (9%)

