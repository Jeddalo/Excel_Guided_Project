# SCOPE
This project carries out data analysis to find answers and provide insights for professionals in that data field. The data gotten from Luke Barousse uses Excel to carry out data analytics process.

## The DataSet Used
The dataset used has gotten from Job Postings has 32,673 rows  that has the following Column:
* Job title
* Job location
* Salary year average
* Job schedule type (full-time, part-time, intership, contractor, and temp work)
* Job skills
* Job posted date

  ## PROCESS
  The following excel tools were a huge part of what was used for the analytics:
  * Formulas and Function
  * Pivots and Charts
  * Data Validation
--
## Formulas and Function
#### Median Salary by Job Title:
To get the median salary of each of the job titles, a separate Excel sheet was used to store the computed data. First, the `unique()` function was used to gather the unique job titles. Then, the following formula & functions were used:


The `median()` function was used along with a nested `if()` function to compute an array of the job title median salaries based on the selected job title, country, job type, and the existence of a yearly salary. The following results have been produced:

The median salaries were then sorted in ascending order so that the job title bar graph can display the results in descending order. Also, 2 other columns were created based on the selected job title so that the bar graph can display the selected job title in dark blue, and the other job titles in light blue.  

Finally, to display the median salary of the selected job title onto the dashboard, the `xlookup()` function was used:


#### Job Count:
To compute the job count of the job title, country, and job type selected, the `count()` function was used with a nested `if()` function. Similar to the median function used, the job title, country, job type, and the existence of a yearly salary conditions were incorporated into the count function.

The formula will produce the resulting array, in which the selected job title count will be displayed on the dashboard through the xlookup function: 




    

