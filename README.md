# Indian Elections Data
This repo includes a normalized list of election results by constituency from all Indian general elections between 1951 - 2019.

## List of Fields

|Field|Data Type|Description|
---|---|---|
|YEAR|integer|Year of the general election in the given constituency. Note that this year reflects the actual date of the election in the constituency.  For instance, several constituencies in Assam and Punjab had their contests for the 1984 election delayed into 1985, so their year is listed as 1985.
|STATE|string|The state of the constituency at the time of the election.
|PC| string |The name of the constituency. Some of these names have been changed from their original 
|NAME| string | Candidate name.
|SEX| string | Sex of the candidate. (Only for elections 1962 - 2009.)
|PARTY| string | Abbreviation of the candidate's party.
|AGE|integer|Age of the candidate at the time of the election. (Only for elections 2004 and 2009.)
|CATEGORY| string |Indicates when a constituency was reserved for Scheduled Caste or Scheduled Tribe candidates. (Only for elections 2004 and 2009.)
|VOTES|integer| Votes for the candidate
|COALITION| string | Candidate's party's coalition name or abbreviation. (See note)
|VOTES_CAST| integer | Total votes cast in the constituency.
|ELECTORS| integer | 1951 - 2009: number of eligible electors in the constituency. 2014 - 2019: total number of votes cast in the constituency (identical to `VOTES_CAST`).

## Notes on Normalization
* State names have been left as they were at election time, *except* for Orissa, which was changed to Odisha in all election years.
* In order to compare constituencies across timeframes, the names of the constituencies have been standardized to their modern names for the following constituncies: Chennai, Kolkata, Mumbai, Thiruvananthapuram, and Vadodara.
* Many other constituencies have slight spelling changes over the years (e.g., "-pore" -> "-pur"). The 2019/most recent spelling is reflected in this data set.
* Major parties and coalitions (notably, Congress -> INC) were converted to their popular abbreviations.  Other parties and most other coalitions were abbreviated with just their first letters.  I couldn't find any instances of conflicts, but this may have resulted in some extremely minor parties being accidentally combined.

## Contributing
There are a number of gaps in the data.  Plus, the sheer volume of data—much of which came from scraped PDF tables—means that there are likely a number of errors or inconsistencies across the years.

If you find an error, or have extra data to add, feel free to open a pull request documenting the changes made.

This data set is currently only available in CSV format, but other file types are also welcome.

## Acknowledgements
* Election data through 2014 from [Bangalore Datameet](https://github.com/datameet/india-election-data).
* Election data 2019 courtesy data scraped by [Anurag Rana](https://github.com/anuragrana/2019-Indian-general-election)
