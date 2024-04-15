# American Dream
## Is the American Dream of home ownership in decline?

### Project Overview:

Housing is a topic that is frequently in the news here in the U.S. Many people have opinions about this topic without consensus. What are the issues, who is faced with the greatest issues because of those issues, and how do we resolve them to name but a few. 

This project will explore static data from the years 2012 and 2022 to determine what has changed, and what has remained the same (or similar). 

### Questions:

-	What is the percentage increase (or decrease) in total housing units from 2012 to 2022.
-	What is the difference in percentage of owner-occupied vs. renter-occupied housing units from 2012 to 2022.
-	Which geographic markets have seen the greatest increase and decrease from 2012 to 2022.
-	Is the perceived increased difficulty in housing affordability based on fact, or is it based on paradigm?
    - “I want to live in a safe area I can afford” vs. “I want to live in New York or San Francisco and can’t afford a safe area there”. 
-	Is it possible to determine whether remote work has had an impact on housing affordability and, if so, what is that impact?

### Data Source: 

-	2022 data.census.gov and 2012 data.census.gov
    - I used the DP04 tables with 5-year estimates. 
    - The U.S. Census Bureau is a government agency; the data source is considered trustworthy.
    - The data was obtained through surveys conducted by the U.S. Census Bureau.
    - It is possible that the two datasets will be combined based on a key field to make analysis easier.


### Data Limitations:

-	This is survey data. Even when collected by the U.S. Census Bureau, the data is subject to nonreporting by some entities. 
-	It appears that data for Puerto Rico is included, in addition to data for all 50 states and the District of Columbia. This will be addressed as part of data wrangling. 

### Ethics and PII:

There was no PII included in either the original datasets, or the created subset. The data was made publicly available by the U.S. Census Bureau. There are no apparent ethical or privacy concerns associated with the use of this data. 

### Data Profile:

-	The original 2022 dataset was in CSV format and was comprised of 574 columns and 3,222 rows, with an additional 2 header rows. The original 2012 dataset was in CSV format and was comprised of 573 columns and 3,221 rows, with an additional 2 header rows.
-	One header row in each dataset was non-descriptive, while the other held very long and somewhat unclear descriptions. 
-	There were multiple duplicated columns and columns in each dataset that held the results of calculations performed by the Census Bureau. 
-	Due to the relatively small size of the dataset, the complexity of the header rows, and the volume of duplicate and unverifiable data fields, the best tool to use for the first pass through data cleaning was Excel. 
    - From each dataset I was able to remove 489 columns, eliminate one header row, and make the remaining field labels more descriptive. 
-	The resulting 2022 dataset was 85 columns and 3,222 rows. The 2012 dataset was 84 columns and 3221 rows. Additional exploration and cleaning will be conducted using Python (one notebook for each dataset until such time as they are joined).
    - The preliminary assumption due to expectations based on the source and collection methodology is that there was nonreporting by some entities. Since this project is designed to compare two points in time, we are only interested in a full join of the two datasets for rows (entities reporting). Any differences will be addressed as part of data wrangling.
      
## Additional Visualization and Presentation

- Link to storyboard is [here](https://public.tableau.com/app/profile/brian.dempster/viz/USHousingProject/Story1?publish=yes)
