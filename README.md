## ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1

<h1 align="center">California ACT & SAT Performance Analysis</h1>

## Purpose

### Problem Statement

In the 2018-19 school year, California had 76 high school districts and 344 unified school districts. This analysis aims to provide an overview of California's standardized test performance, and identify the state’s worst-performing counties, districts and subjects. This will allow the state to better understand their academic performance, and see where additional resources are required.

### Background

The SAT and ACT are standardized tests that many colleges and universities in the United States require as part of their admissions process. The test scores are used alongside grade point averages (GPA) and essay responses to determine whether or not the applicant will be granted admission.

The ACT has four sections: English, Math, Reading, and Science, with an additional optional writing section. The composite benchmark score is 21.

The SAT has two sections: Evidence-Based Reading and Writing and Math. Both sections have scores ranging from 200 to 800, with a total possible combined score of 1,600. For grade 12, the Evidence-Based Reading and Writing section benchmark score is 480, and the Math section benchmark score is 530.

Since the 1940's, an increasing number of colleges have been using these standardized test scores as a measure for college readiness and aptitude. However, in recent years, it's been questioned as to whether or not it accurately reflects a student's potential, and whether or not using them is fair, given that a student's performance largely depends on the quality of education and resources made available to them through the education system.

As a result, higher education schools are beginning to drop the ACT/SAT requirement on their applications, but these tests are maintaining their presence. Therefore, secondary education systems must continue their efforts in providing the necessary resources to prepare their students for these standardized tests.

---

## Data

### Datasets

*2019 ACT Scores in California by School*
* Contains the average scores by test section (English, Reading, Math and Science) and the percentage of participants whose composite scores were greater or equal to 21 for the test administration year 2018-19. This information is according to school, for which  the district and county name are noted, if available.
* The original dataset contained 2,310 observations and 18 features. After removing schools with null values and columns without relevant information, the dataset was reduced to 1,367 rows and 13 features.

*2019 SAT Scores in California by School*
   * Contains the percent of participants who met or exceeded the benchmark for Evidence-Based Reading & Writing and Math, both individually and together, the test administration year 2018-19. This information is according to school, for which  the district and county name are noted, if available.
   * The original dataset contained 2,580 observations and 26 features. After removing schools with null values and columns without relevant information, the dataset was reduced to 1,667 rows and 13 features.

### Data Dictionary

|**Feature**|**Type**|**Dataset**|**Description**|
|---|---|---|---|
|**school_name**|*object*|ACT/SAT|The school name.|
|**district_name**|*object*|ACT/SAT|The district name.| 
|**county_name**|*object*|ACT/SAT|The county name.|
|**grade_12_enrollment**|*float*|ACT/SAT|The enrollment of grade 12.| 
|**total_num_test_takers**|*float*|ACT/SAT|The number of participants.| 
|**avg_reading**|*float*|ACT|Average ACT Reading score.|
|**avg_english**|*float*|ACT|Average ACT English score.|
|**avg_math**|*float*|ACT|Average ACT Math score.|
|**avg_science**|*float*|ACT|Average ACT Science score.|
|**num_test_takers_21**|*float*|ACT|The number of participants whose ACT Composite Scores are greater or equal to 21.| 
|**pct_test_takers_21**|*float*|ACT| The percent of participants whose ACT Composite Scores are greater or equal to 21.| 
|**num_erw_benchmark**|*float*|SAT|The number of participants who met or exceeded the benchmark for Evidence-Based Reading & Writing (ERW) test for Grade 12.
|**pct_erw_benchmark**|*float*|SAT|The percent of participants who met or exceeded the benchmark for Evidence-Based Reading & Writing (ERW) test for Grade 12.
|**num_math_benchmark**|*float*|SAT|The number of participants who met or exceeded the benchmark for the SAT Math test for Grade 12.
|**pct_math_benchmark**|*float*|SAT|The percent of participants who met or exceeded the benchmark for the SAT Math test for Grade 12.
|**num_test_takers_benchmark**|*float*|SAT|The total number of participants who met the benchmark of both Evidence-Based Reading & Writing (ERW) and Math Grade 12.| 
|**pct_test_takers_benchmark**|*float*|SAT|The percent of participants who met the benchmark of both Evidence-Based Reading & Writing (ERW) and Math Grade 12.| 
|**year**|*object*|ACT/SAT|The test administration year.| 

### Definitions

   * **Overall:** All schools with recorded test data.

   * **Worst-Performing:** Schools where less than 10% of participants met or exceeded the benchmark score.

   * **Benchmark Participant:** Participants who met or exceeded the benchmark score.

---

## Exploratory Data Analysis

### ACT vs. SAT Performance by District

Between the ACT and SAT, the ACT had more districts with higher benchmark student percentages giving it more of a left-skewed distribution, while the SAT held more of a normal distribution with more districts concentrated in the middle percentiles.

In the ACT dataset, there were 353 districts represented and 29 (8%) of those had schools with less than 10% benchmark participants. In the SAT dataset, there were 406 districts represented and 38 (9%) of those had schools with less than 10% benchmark participants.

Between the ACT and SAT datasets, there were 52 distinct districts and there was a heavier concentration of these worst-performing districts in 3 counties: Los Angeles, Fresno and Riverside. Respectively, they claim 11, 6, and 6 worst-performing districts, and together they make up 44% of the worst-performing districts.

### ACT vs. SAT Performance by Subject

The ACT dataset provided each school's average score by subject, through which the state's average score by subject was determined, and are as follows: Reading (22), English (21), Math (21) and Science (21). The worst-performing schools' averages are: Reading (16), English (14), Math (16) and Science (16).

Based on these averages, there is no subject that can be considered worst-performing, either overall or at worst-performing schools.

The SAT dataset provided each school's percent of participants who met or exceeded the benchmark, through which the state's average percent of participants who met or exceeded the benchmark was determined, and are as follows: Evidence-Based Reading & Writing (68%) and Math (46%). The worst-performing school's averages are: Evidence-Based Reading & Writing (27%) and Math (7%).

Based on these averages, Math is the subject that is giving participants much difficulty, both overall and at worst-performing schools.

---

## Conclusion

### Recommendations

With 52 worst-performing districts, California has some academic improvements to consider. To start, focusing on the districts in the top 3 counties with the most number of worst-performing districts (Los Angeles, Fresno and Riverside), will have the highest impact as they make up 44% of the worst-performing districts. These counties/districts will require a higher quality of instruction and delivery style with an emphasis on Math.

### Next Steps

A separate analysis will be beneficial to assess the current quality of instruction and delivery style at these worst-performing districts. This will be to determine what exactly needs to be implemented and/or changed so that the state can make an efficient use of its resources. 