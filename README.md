# Excel Salary Dashboard

<img width="1129" height="524" alt="Image" src="https://github.com/user-attachments/assets/732d3765-c47a-40aa-b7bd-5174c1ed72fb" />


# SCOPE
This project carries out data analysis to find answers and provide insights for professionals in the data field. The project creates an interactive Salary dashboard that helps professional Job seekers investigate their desired job and ensure that they are getting adequately compensated.The data gotten from Luke Barousse uses Excel to carry out data analytics process.


## The DataSet Used
The dataset used has gotten from Job Postings has 32,673 rows  that has the following Column:
* Job title
* Job location
* Salary year average
* Job schedule type (full-time, part-time, intership, contractor, and temp work)
* Job skills
* Job posted date

# Dashboard File
My Final dashboard is in 

  ## PROCESS
  The following excel tools were a huge part of what was used for the analytics:
  * **🧮 Formulas and Function**
  * **📉 Pivots and Charts**
  * **❎ Data Validation**

## Dashboard Build
## 📉 Charts
#### 📊 Data Science Job Salaries - Bar Chart

<img width="365" height="251" alt="Image" src="https://github.com/user-attachments/assets/b947cc58-5240-4556-b80c-7a0e61de7e33" />
<img width="365" height="251" alt="Image" src="https://github.com/user-attachments/assets/c33dae55-4628-4c93-8fa2-09e0480656c4" />


Horizontal bar charts were plotted to illustrate the results of the job count, median salaries and job platform based on the selected job title, country, and job type.
* In both bar charts, the selected job title and job type are bolded, which users can easily compare their selected job title and job type with the other ones.
* The job titles and job type are sorted by descending salary, which users can easily identify the highest and lowest job salaries and job type amount.
* From the bar charts above, it is revealed that senior and engineer roles are higher paying than analyst roles, and that the majority of the job types are full-time.

  ### ### 🧮 Map Chart

  <img width="333" height="237" alt="Image" src="https://github.com/user-attachments/assets/2739ec8d-9f31-43b8-a921-a301bc1c0abe" />

  A map chart was plotted to identify the countries with the highest median salaries based on the selected job title and job type. 
* The countries from the map chart are color coded where the ones with a darker blue color are the ones with the higher median salaries, and the countries in grey are ones with no jobs available of the selected job title and type.
* Users can easily differentiate and compare the job salaries of each country, and can move the cursor towards a certain country to display its exact median salary
* For full-time data analyst positions, from the map above, the cursor is on the United States country where it displays the median salary to be $90,000. Also, the country that is dark blue is Belarus, which has the highest median salary of $400,000.


## Formulas and Function
#### Median Salary by Job Title:
To get the median salary of each of the job titles, a separate Excel sheet was used to store the computed data. First, the `unique()` function was used to gather the unique job titles. Then, the following formula & functions were used:


```
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```

The `median()` function was used along with a nested `if()` function to compute an array of the job title median salaries based on the selected job title, country, job type, and the existence of a yearly salary. The following results have been produced:

<img width="270" height="216" alt="Image" src="https://github.com/user-attachments/assets/9d0e5616-f4c7-4e8b-ab01-0bf685261f97" />

The median salaries were then sorted in ascending order so that the job title bar graph can display the results in descending order. Also, 2 other columns were created based on the selected job title so that the bar graph can display the selected job title in dark blue, and the other job titles in light blue.  

<img width="399" height="196" alt="Image" src="https://github.com/user-attachments/assets/81d610e6-ad2f-41f9-9093-14956a089340" />

To display the median salary of the selected job title onto the dashboard, the `xlookup()` function was used:


#### Job Count:
To compute the job count of the job title, country, and job type selected, the `count()` function was used with a nested `if()` function. Similar to the median function used, the job title, country, job type, and the existence of a yearly salary conditions were incorporated into the count function.

```
COUNT(
  IF(
    (jobs[job_country]=country)*
    (jobs[job_title_short]=A2)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type]))),
    jobs[salary_year_avg]
  )
)
```
The formula will produce the resulting array, in which the selected job title count will be displayed on the dashboard through the xlookup function: 

<img width="259" height="222" alt="Image" src="https://github.com/user-attachments/assets/d0f3af9f-e650-4bdf-898c-672c6d4398fc" />

## Conclusion

I created this dashboard to showcase insights into salary trends across various data-related job titles. Utilizing the data, this dashboard allows users to make informed decisions about their career paths. Exploring the functionalities to understand how location and job type influence salaries.




    

