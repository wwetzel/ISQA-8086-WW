## Crime in Nebraska

#### General Description

[This data](https://ncc.nebraska.gov/stat-reports#Crime_in_Nebraska_Series) includes tables of information about crimes committed in Nebraska, law enforcement employment statistics, and traffic stop information.  There are reports from 1995 to 2016, with the same data present in each report.  The data sits between fully summarized and raw data - there are crime statistics by crime type, city size, age group of offenders, and location.  

Interesting insights could come from combining 10+ years of data.  I would combine other historical annual data sets such as economic indicators, to try and find correlations to Nebraska crime statistics for that year.  This data set could be interesting when analyzed with a time-series analysis or regression to predict future crime rates.             

#### Data Description

The data is published on the Nebraska Crime Commission website in pdf from.  Each pdf contains multiple tables of information.  There are about 30 variables contained across the pdfs which could be combined into a single matrix.  Multiple years of crime data can be combined into a single matrix, adding additional variables and forcing a decision on how to best organize it.  When all datasets are combined, I estimate a matrix would be roughly 750x30 in size. 

At a glance data categories include: 
* Total instances of crimes committed based on city size
* Suspect age 
* If the incident was a hate crime
* Location of the crime
* Officer employment
* Traffic stop geolocation data
* Traffic stop reasons
* Crime type by city type
* Crime locations

The main challenge would be removing the table data from the pdfs and combining them successfully into one data set, for the 10+ years of data one would extract.  It may be possible to email an employee at the state and request the data in a different format.

#### License

This data may fall under two licenses.  The Nebraska Crime Commission site does not appear to display an explicit license for data usage.  Looking at the "Use of Site Information" on the "Policies" page, we find the [quote](http://www.nebraska.gov/policies/):

> "You may access, copy, download, and print the material contained on the Site for your personal and non-commercial use, provided you do not modify or delete any copyright, trademark or other proprietary notice that appears on the material you access, copy, download or print." 
  
I believe this data may also fall under a [U.S. Government Works](https://www.usa.gov/government-works) license, meaning as they were prepared by officers of employees of the United States government there is generally no copyright on such published works.

#### Potential Data Users


Crime and incarceration are topics of interest in most societies.  This data would be used by high and low level politicians to make a point or further an agenda, and reviewed by government workers in multiple departments to analyze Nebraska crime against other factors.  As machine learning and predictive analytics become topics of interest for governments, crime statistics similar to these could be used to predict crime rates or train a model.  

Private organizations such as the ACLU or anyone involved in a lawsuit with the state of Nebraska may obtain and reference findings in the crime dataset.  Researchers or medical professionals may be interested in tracking crime data as it impacts their professional work.  

#### Questions this Data May Answer

1. How do police staffing rates (overtime, understaffed, etc.) impact annual state crime rates?
 * This data is contained in the Law Enforcement Employment dataset.
2. How closely do a city's crime rates, follow state crime trends year over year?
 * To answer this you would need to find city crime data for Nebraska cities.
3. What types of crime does increased traffic stop frequency impact the most?
 * This data is contained in the Traffic Stop dataset.

Ideas of external data sets that would be interesting to combine with:

1. [City of Omaha Crime Statistics](https://police.cityofomaha.org/crime-statistics/)
2. Nebraska Census Data of people moving into and out of the state
3. Historical Economic Data
 * Inflation and Consumer Price Indexes
 * Jobs growth or shrinkage
 * Stock market KPIs
4. Crime data from other states 

#### APA Citation

Nebraska Crime Commission Stat Reports [Online Database]. (2017, January 01). Retrieved September 4, 2017, from https://ncc.nebraska.gov/stat-reports#Crime_in_Nebraska_Series


