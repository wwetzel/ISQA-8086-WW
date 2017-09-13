Will Wetzel  
ISQA 8086  
September 13th, 2017  
Data Entry Analysis  
Problems in Planktontown

### Problems Discovered in Data Sets

1. None of the 3 spreadsheets have a primary key column, this is going to make accessing specific fields difficult.  Adding a timestamp type column to this dataset could help greatly.
 * For this reason the "pond2010" data set is unusable, you can't tell which cuni and chippo observations happened at the same time, as there are 15 per day - and the most precise time measurement we have is by the day.
2. The spreadsheet names, "zoop - temp", "zoop - temp-main", "pond2010" are generally meaningless.  A readme file should have been included with this data set to explain all variables and spread sheets.
  * More specifically, between "zoop - temp", and "zoop - temp-main", there are observations which look identical, yet some are different. The titles would suggest these two documents are backups of each other.  We would have a difficult time knowing how to treat these two dataframes without further input from the domain expert on how they should be used.
3. The column "Chla" is present in both "zoop" datasets, but not in "pond2010" - although the 3 tables appear to be recording the same data, the "Chla" column doesn't appear to be shared.
4. In "zoop -temp" there are comments and random fields filled in that do not pertain to the scientific measurements dataframe.  If you wanted to analyze this data, you would need to clean out all of the notes before using most statistical software packages.  It would be better to leave this data in a readme, especially if it is a production dataset. 
5. The background on the data states "Frequently, aquatic scientists collect plankton samples during both day (e.g. noon) and night (e.g. 2 am) because plankton change their distributions from day to night".  While there are 15 observations per day in the data set, we have no way of knowing at what time they were made.  As the scientists hope to study the day vs night distribution of plankton, they may want to record at what time they are taking their measurements.
6. The "Temp" column in two of the spreadsheets has null values, and one has an asterick mixed with floats.  Null values speak to a data collection problem, but there should not be '*' in with numbers in a column.
7. The "pond2010" spreadsheet has a column named 'z', based off the name alone you could never guess what it is referring to.  
8. Units are missing from multiple columns in the data set, we don't know if 'Temp' is Fahrenheit or Celsius.  Cuni/Chippo ColonySize have no units.  A data dictionary would help here - I'm not sure how appropriate it is to leave units in the column name generally.
9. Column names should probably be more analysis oriented, if someone were to write R scripts to analyze this data, it's not intuitive to call columns things like "Chippo #/L" - "chippo_num_large" is easier from that perspective.

### Proposed Data Organization Example

|Timestamp|Depth (m)|Temp (C)|cuniDensity (mol/L)|cuniDiameter (cm)|chippoDensity (mol/l)|chippoDiameter (cm)|Chla???|
|---|---|---|---|---|---|---|---|
|2017-13-09:15:23:42.545321|0.5|14.2|72|2.13|45|2.53|3.1|

### Proposed Data Organization Explanation

While there are some obvious improvements to be made in organizing the dataset - there are questions you would want to ask stake holders to get a better idea of how they may be analzying the data, and if there is industry standard terminology.  I tried to focus on the obvious ones, while not making too many assumptions about the nature of their experiment or the 'business rules' of this case.  The column "Chla???" was included to indicate I don't know if it's a required data point or not.

I think it makes more sense to use different columns for 'Chippo' and 'Cuni' colony sizes and density, scientists may be interested in the different distribution of the two plankton over time.  By having the two factors as columns, we can use the timestamp as a primary key (assuming measurements are made at the same time).  The use of the words 'Density' and 'Diameter' in the 'pond2010' dataframe seemed more clear than 'ColonySize' and '#/L' present in the other data sets.  I have decided to fill in sample units where applicable, I tried to compromise between programming and business friendly column names, you would need to decide this based on future usage of the data.  Most of these concerns I think would be best addressed by a data dictionary.

