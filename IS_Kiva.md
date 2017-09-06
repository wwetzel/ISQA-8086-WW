## Kiva API

#### General Description

[Kiva](https://www.kiva.org/about) in a not-for-profit 2005 silicon valley startup which provides micro loans to recipients across the world, primarily in third world countries.  Their development team built the Kiva API for individuals to expand the reach of Kiva to new audiences.  According to their metrics, they have reached 2.5 million borrowers in 84 countries with 1.03 billion dollars.  Data is organized by continent, with various types of businesses receiving funding.  Part of my interest in selecting this data set is the use of an API for data acquisition.   

#### Data Description

Data can be retrieved in JSON, XML, or HTML format, using the Kiva API.  The API is a REST web-service, utilizing HTTP requests and responses to retrieve data.  The best way to utilize this data would be predefining a subset of demographics whom you want to analyze.  Some examples would be female entrepreneurs in Africa, or grocery businesses in South America.

Available variables include information found throughout the site - some main categories include:
 * Loan Details
 * Borrower and Lender Information
 * Loan Updates/Journal Entries
 * Location   

Due to the volume of data available throughout the API, it would be pertinent to clearly define your selection criteria prior to beginning data extraction.

#### License

The API administrators are adamant about developers reading the ["Kiva Developer Terms of Service"](http://build.kiva.org/docs/tos) before using the service.  I've read the terms, and highlighted the relevant portions here:

> "...Kiva grants Licensee a non-exclusive, revocable, nonsublicensable, nontransferable license to use the Kiva API and API Materials (collectively referred to as the “Licensed API”) to develop, reproduce and distribute non-commercial applications for the Permitted Purpose (“Developed Applications”)"

> "Licensee may not use the Licensed API or any Kiva data, information or materials for any other purpose (including without limitation any commercial purpose) other than the Permitted Purpose without Kiva’s prior written consent. Further, under no circumstances will Licensee benefit commercially or financially from a Developed Application or any Kiva information, data or materials."

Other relevant sections include "4. Other Restrictions" and "6. Additional Licensee Obligations", which details concepts such as not modifying the API and building applications which "...preserve the dignity of all persons."  I believe a research-driven, academic use of their data fall well within the defined terms of use.


#### Potential Data Users

Kiva has a wide enough reach that the data it collects about its partner outcomes, loan repayment rates, and benefits of microlending, would be useful to other non-profits operating in a similar space.  NGOs and other micro lenders need to consistently evaluate outcomes and adjust their strategies.  Kiva data could inform lending and general economic strategy when it comes to attempting to kick-start a third world economy.

Governments or non-profits of countries where Kiva lends could obtain data about how to better serve their underprivileged citizens.  Economic analysts could use this data to better understand the entrepreneurial environment of a given country, and view difficult to track segments of the economy.       


#### Questions this Data May Answer

1. What is the most common type of business requesting funding in countries which have had a significant conflict in the past 10 years?
 * We could hypothesize that countries which have recently undergone an armed conflict are more in need of certain services.  To do this analysis we would need historical conflict information for regions we were interested in.
2. What African country receives the highest percentage of funded micro loans?
 * By examining the disparity in loans awarded by country, we can understand how micro lending impacts different population, and asses lending partner efficacy.
3. What percentage of micro loan recipients receive at least one additional micro loan within 5 years by country?
 * We could begin to understand the fiscal outcomes of loan recipients by examining how many loans a business owner will need to take. 


#### APA Citation

Kiva API [Online Database]. (2013, February 19). Retrieved September 4, 2017, from http://build.kiva.org/docs/


