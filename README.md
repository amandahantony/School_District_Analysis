# School_District_Analysis
Performing an updated analysis on student and school data using Pandas. 

## Overview of Project 
### Purpose
In this project, we helped Maria alter and analyze school and student datasets to produce meaningful information about reading and math scores in relation to each school's overall performance, spending, size and type. The final code also ommitted grade 9 reading and math scores from Thomas High School on suspicion of academic dishonesty. The final code and analysis will be used by Maria and the school board to get a better understanding of the district's performance, while avoiding possible incorrect values but keeping all other data intact.

## Results 
This updated analysis slightly varies from the initial analysis ([Original School District Analysis](PyCitySchools.ipynb)) as the reading and math scores from Thomas High School's grade 9 was replaced with NaN (Not a Number), but leaving all other data intact. Below is a screenshot that shows the replacement of selected data with NaN.
![Selected Data Replaced with NaN](Other/Refactored_Code_Arrays.png)

1) In the refactored code I created 3 additional arrays (as shown below): tickerVolumes, tickerStartingPrices and tickerEndingPrices. The tickers array from the original code was also used in the refactored code. A tickerIndex variable was created to access the correct stock ticker index in each array.**
###### Refactored Code and Arrays
![Refactored Code and Arrays](Other/Refactored_Code_Arrays.png)
