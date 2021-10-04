# BootCamp-Mod-4-School_District_Analysis
Analyzing school district and standardized testing data from 15 high schools .

## Overview of Project
### Purpose
The purpose of this analysis is to use Pandas to help Maria, the chief data scientist for a city school district, show student performance trends and patterns to the school board and superintendent to determine which schools need additional support and determine how removing all of the student information from one of the grades of one of the schools will affects the analysis.

## Analysis and Challenges
### Data
Two sources of data were provided:
- Information about 15 schools in the district, which includes whether the school is a district school or charter school, the number of students in each school, and the budget each school has.
- Information about the student performance on math and reading standardize tests, including their score for each test, which school the student goes to, and what grade each student is in.

These two sources were then merged together in to a Pandas DataFrame so that all calculations and analysis can be performed on one source of data.

### Cleaning and Organizing the Data
Before any analysis can begin, the data must be cleaned. 
- Step. 1 - Remove any student prefixes and suffixes that do not correspond to their actual name, such as Dr. or DDS.
- Step. 2 - Determine some basic calculations to be able to compare the schools (referred to as "the 5 number school report" for the rest of this analysis).
  * The average student math score for each school.
  * The average student reading score for each school.
  * The percentage of students who passed the math test.
  * The percentage of students who passed the reading test.
  * The percentage of students who passed both tests.

### Initial Analysis
Analysis was performed on data to determine:
- The 5 schools with the highest percentage of students who passed both tests.
- The 5 schools with the lowest percentage of students who passed both tests.
- The math and reading score averages broken down by school and grade.
- The 5 number school report broken down by the school budget per student.
- The 5 number school report broken down by the school size.
- The 5 number school report broken down by the type of school.

### Replacing Thomas High School Grade 9 Test Scores
- The school board determined evidence of academic dishonesty among the 9th grade students of Thomas High School and wanted their test score information removed from the analysis.
- Using the loc method, Pandas is able to locate all of the students in data who are 9th grade students of Thomas High School and replace them with NaN values. 

### Reanalyzing the data
- The same analysis was run on the data with the NaN values to determine which 


## Results
### District Summary
- Looking at the District Summary before and after taking the Thomas High School 9th grade data out:
 * The average math score for the district went down one-tenth of a point, causing the percent of students who passed the math test to decrease by two-tenths of a percentage.
 * The average reading score did not change enough to show a change to the nearest tenth. However, we do see that it changed slightly since, the percent of students who passed the reading test decreased by one-tenth of a percentage.
 * These changes caused the percent of students who passed both tests to decrease by three-tenths of a percentage.

<p align="center">Before<img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/Old_District_Summary.png"/>After<img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/New_District_Summary.png"/></p>

### School Summary
- The school summary did not change, except for the values for Thomas High School, since this information is broken down by school. Therefore, the changes to the Thomas High School data does not effect this summary.
- At first, it seemed that the percentage values for Thomas High School changed drastically as shown below. However, this was before the values were adjusted to divide by the number student in only the 10th, 11th, and 12th grade instead of the total number of students in the school. 

<p align="center">Before<img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/Old_Schools_Summary.png" width="474" height="408"/>&nbsp;&nbsp;After<img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/New_Schools_Summary.png" width="474" height="408"/></p>

- After calculating the values for Thomas High School based only on the number of 10th, 11th, and 12th graders, the values did not change much.
 * The average math score decreased by less than a 10th of a point and the percentage of students who passed the math test decreased by less than one-tenth of a percent
 * The average reading score decreased by less than a 10th of a point and the percentage of students who passed the reading test decreased by less than two-tenths of a percent.
 * The percentage of students who passed both tests decreased by slightly over three-tenths of a percent.

<p align="center">Before<img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/Old_Schools_Summary.png" width="474" height="408"/>&nbsp;&nbsp;After<img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/Corrected_Schools_Summary.png" width="474" height="408"/></p>

### Thomas High School Performance
- The ranking of the schools was determined by the percentage of students who passed both tests.
- Before removing the 9th grade data, Thomas High School was the second highest school.
- After removing the 9th grade data, even though their percentage dropped slightly, Thomas High School is still the second highest school.

<p align="center">Before - Top 5<img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/New_Top_5.png"/>Before - Bottom 5<img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/Old_Top_5.png"/>After - Top 5<img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/Old_Bottom_5.png"/>After - Bottom 5<p align="center"><img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/New_Bottom_5.png"/></p>

### Math and Reading Score Summaries
- The Math and Reading Scores did not change since the data was broken down by school and grade.
- The only difference is that the values for Thomas High School 9th grade are now nan.

<p align="center">Math</p>
<p align="center"><img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/Old_Math_by_Grade.png" width="246" height="340"/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/New_Math_by_Grade.png" width="246" height="340"/></p>

<p align="center">Reading</p>
<p align="center"><img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/Old_Reading_by_Grade.png" width="246" height="340"/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/New_Reading_by_Grade.png" width="246" height="340"/></p>

### Scores by School Spending
- From the formatted summary chart, it looks like replacing the Thomas High School 9th grade data did not change the summary by school spending did not change.

<p align="center">Before<img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/Old_per_Capita_Summary_Formatted.png"/>After<img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/New_per_Capita_Summary_Formatted.png"/></p>

-Looking at the unformatted data, we see that in the $630 - 644 range, we can see slight changes less than one-tenth of a point or percentage for all of the values of the 5 number school report.

<p align="center">Before<img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/Old_per_Capita_Summary.png"/>After<img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/New_per_Capita_Summary.png"/></p>

### Scores by School Size
- From the formatted summary chart, it looks like replacing the Thomas High School 9th grade data did not change the summary by school size did not change.

<p align="center">Before<img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/Old_size_summary_Formatted.png"/>After<img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/New_size_summary_Formatted.png"/></p>

-Looking at the unformatted data, we see that in the medium range, we can see slight changes less than one-tenth of a point or percentage for all of the values of the 5 number school report.

<p align="center"><img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/Old_size_summary.png"/><img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/New_size_summary.png"/></p>


### Scores by School Type
- From the formatted summary chart, it looks like replacing the Thomas High School 9th grade data did not change the summary by school type did not change.
- 
<p align="center"><img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/Old_type_summary_Formatted.png"/><img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/New_type_summary_Formatted.png"/></p>

-Looking at the unformatted data, we see that in charters, we can see slight changes less than one-tenth of a point or percentage for all of the values of the 5 number school report.

<p align="center"><img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/Old_type_summary.png"/><img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/New_type_summary.png"/>&nbsp;</p>

### Challenges
- The most difficult part of this challenge was only seeing the formatted summaries at first. Because the values did not change, I thought that there was an issue with the code. I went back and spent some time trying to debug the code. Then, when I printed the unformatted summaries, I realized that the changes were so small that the rounding obscured these minor changes.

## Summary
- In summary, after removing the Thomas High School grade 9 data, 4 changes were discovered in the summaries.
  * The values for Thomas High School decreased.
  * The values for schools with the $630 - 644 range for spending decreased.
  * The values for medium schools decreased.
  * The values for charter schools decreased.
- However, none of these changes made any significant changes to the summaries.
- Thomas High School remained the second top school.

