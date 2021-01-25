# School_District_Analysis
Performing an updated analysis on student and school data using Pandas. 

## Overview of Project 
### Purpose
In this project, we helped Maria update and analyze school and student datasets to produce meaningful information about reading and math scores in relation to each school's overall performance, spending, size and type. The updated code also ommitted grade 9 reading and math scores from Thomas High School on suspicion of academic dishonesty. The updated summaries will be used by Maria and the school board to get a better understanding of the district's performance, while avoiding possible incorrect values but keeping all other data intact.

## Results 
This updated analysis slightly varies from the initial analysis ([Original School District Analysis](PyCitySchools.ipynb)) as the reading and math scores from Thomas High School's grade 9 was replaced with NaN (Not a Number), but leaving all other data intact. Below is a screenshot that shows the replacement of selected data with NaN, after using the numpy.nan or np.nan function.

![Selected Data Replaced with NaN](Images/SelectedDataReplaced_with_NaN.png)

1) The district summary provided information on the total number of schools, students and budget in the district, average math and reading scores across the district, as well as the percentage of passing students. The district summary from the updated analysis (as shown below), remained the same as the original analysis except for one value, average math score. The average math score in the updated analysis decreased by 0.1% in comparison to the original. 

![District Summary](Images/District_Summary.png)

2) The school summary provided information on the size, type, budget, average scores and percentage passing for each school. The school summary from the updated analysis (as shown below), was significantly altered in comparison to the original analysis. Once the reading and math scores from Thomas High School grade 9 was replaced with NaN, the % Passing Math, % Passing Reading and % Overall Passing went down to 66.9%,	69.7% and 65.1%, respectively. These are over 20% lower than in the original analysis. Before the values were replaced, the % Passing values were all above 90%. The other values remained the same. 

![School Summary](Images/school_summary.png)

3)Replacing the ninth graders' math and reading scores significantly lowered Thomas High School's overall performance. Prior to replacement, Thomas High School was in the top 5 schools based on % Overall Passing. After replacement, Thomas High School went down to 8th place out of 15 schools. Shown below is the ranking of the schools after replacement of Thomas High School's ninth graders' math and reading scores, after using the sort_values function. 

![Ranking After Replacement](Images/Ranking_after_Replacement.png)

4)Both the reading and math scores by grade were not affected by the replacement for grades 10 through 12. However, the reading and math scores for ninth graders at Thomas High School was marked as nan. This is understandable as we had replaced those values with NaN at the beginning of the project. Shown below are the reading and math scores by grade with school name being the index. 

![Reading Score by Grade](Images/reading_scores_bygrade.png) ![Math Score by Grade](Images/math_scores_bygrade.png)

5)School spending was divided into 4 bins determined by the minimum, maximum and standard deviation values. These values were retrieved by applying the describe() function to the budget per student. After replacing the ninth-grade scores, the % passing math, % passing reading, and % overall passing values changed, but only within the $630-644 bin. This makes sense because the per student budget for Thomas High School is $638, which is between $630 and $644. The % passing math value decreased by 6%, % passing reading decreased by 7%, and % overall passing decreased by 7%. The scores by school spending data frame is shown below.

![Score by Spending Range](Images/scoreby_spendingrange.png)

6)School size was divided into 3 bins; small, medium and large. After replacing the ninth-grade scores, the % passing math, % passing reading, and % overall passing values changed, but only within the medium bin (1000 - 2000). This makes sense because the total students at Thomas High School is 1635. The % passing math, % passing reading and % overall passing values all decreased by 6%. The scores by school size data frame is shown below.

![Score by School Size](Images/scoreby_schoolsize.png)

7)School type was divided into two; Charter and District. After replacing the ninth-grade scores, the % passing math, % passing reading, and % overall passing values changed, but only within the Charter type. This makes sense because Thomas High School is within the Charter type. The % passing math value decreased by 4%, % passing reading decreased by 4%, and % overall passing decreased by 3%. The scores by school type data frame is shown below.

![Score by School Type](Images/scoreby_schooltype.png)


** In the second half of deliverable 2, we calculated a new student count that only included students from grade 10 to grade 12 at Thomas High School. The school summary dataframe was updated to now include % passing values that were calculated based off of the new student count. The new school summary dataframe now looks very similar to the original school dataframe, with values being only a few decimals off. Eliminating the grade 9 scores and altering the student count accordingly, made a miniscule change to the overall school summary. 

## Summary
As a result of the school board suspecting academic dishonest within Thomas High School ninth graders, we replaced their reading and math scores wit NaN. Upon making this alteration to the code, there were a few changes to the summaries. However, the changes only applied to the % passing values. Budgets, type, student size and average scores remained the same. The overall school summary showed that when the scores were replaced, Thomas High School's ranking fell down 6 places. This was a result of the 26% decrease in % Passing math, 28% decrease in % Passing reading, and 26% decrease in % overall passing. Additionally, the % passing values within the third bin of school spending, $630 - 644, decreased by around 6-7%. The % passing values within the second bin of school size, medium (1000 - 2000), decreased by 6%. Finally, the % passing values decreased by about 3-4% within the charter type schools, because of this replacement. 
