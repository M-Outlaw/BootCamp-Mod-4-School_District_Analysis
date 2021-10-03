# BootCamp-Mod-4-School_District_Analysis
Analyzing school district and standardized testing data from 15 highschools .

## Overview of Project
### Purpose
The purpose of this analysis is to use Pandas to help Maria, the chief dagta scientist for a city school district, show student performance trends and patterns to the school board and superintendent to determine which schools need additional support and determine how removing all of the student information from one of the grades of one of the schools will affects the analysis.

## Analysis and Challenges
### Data
Two sources of data were provided:
- Information about 15 schools in the district, which includes whether the school is a distric school or charter school, the number of students in each school, and the budget each school has.
- Information about the student performance on math and reading standardize tests, including their score for each test, which school the student goes to, and what grade each student is in.

These two sources were then merged together in to a Pandas DataFrame so that all calculations and analysis can be performed on one source of data.

### Cleaning and Organizing the Data
Before any analysis can begin, the data must be cleaned. 
- Step. 1 - Remove any student prefixes and suffixes that do not correspond to their actual name, such as Dr. or DDS.
- Step. 2 - Determine some basic calculations to be able to compare the schools (refered to as "the 5 number school report" for the rest of this anlaysis).
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

### Reanalysing the data
- The same anlysis was run on the data with the NaN values to determine which 


## Results
### District Summary


<p align="center"><img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/New_District_Summary.png"/>&nbsp;<img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/Old_Distric_Summary.png"/></p>

### School Summary


<p align="center"><img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/New_Schools_Summary.png"/>&nbsp;<img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/Old_Schools_Summary.png"/></p>

### Thomas High School Performance

###



<p align="center"><img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/New_Top_5.png"/>&nbsp;<img src="
https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/Old_Top_5.png"/></p>




<p align="center"><img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/New_Bottom_5.png"/>&nbsp;<img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/Old_Bottom_5.png"/></p>







<p align="center"><img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/New_Math_by_Grade.png"/>&nbsp;<img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/Old_Math_by_Grade.png"/></p>


<p align="center"><img src="
https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/New_Reading_by_Grade.png"/>&nbsp;<img src="
https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/Old_Reading_by_Grade.png"/></p>










<p align="center"><img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/New_per_Capita_Summary_Formatted.png"/>&nbsp;<img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/Old_per_Capita_Summary_Formatted.png"/></p>

<p align="center"><img src="
https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/New_size_summary_Formatted.png"/>&nbsp;<img src="
https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/Old_size_summary_Formatted.png"/></p>



<p align="center"><img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/New_type_summary_Formatted.png"/>&nbsp;<img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/Old_type_summary_Formatted.png"/></p>





<p align="center"><img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/New_per_Capita_Summary.png"/>&nbsp;<img src="
https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/Old_per_Capita_Summary.png"/></p>


<p align="center"><img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/New_size_summary.png"/>&nbsp;<img src="
https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/Old_size_summary.png"/></p>


<p align="center"><img src="
https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/New_type_summary.png"/>&nbsp;<img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/Old_type_summary.png"/></p>












<p align="center"><img src="https://github.com/M-Outlaw/BootCamp-Mod-2-Stock-Analysis/blob/main/Resources/Runtime_Before_Refactoring_2017_.png" width="371" height="127"/>&nbsp;<img src="https://github.com/M-Outlaw/BootCamp-Mod-2-Stock-Analysis/blob/main/Resources/Runtime_Before_Refactoring_2018.png" width="371" height="127"/></p>

<p align="center"><img src="https://github.com/M-Outlaw/BootCamp-Mod-4-School_District_Analysis/blob/main/Resources/Corrected_Schools_Summary.png" width="740" height="360"/></p>

- **Note:** If the candidate percentages are totaled, it only equates to 99.9% of the votes. This is not an error and is not an issue for concern. It is a product of rounding for the output to look cleaner. If the rounding were taken off, the percentages would total to exactly 100%.

## Election-Audit Summary
- In summary, this Python code provided accurate information about this U.S. Congressional election for a precinct in Colorado. Through a few easy changes the code can be changed to work for any election.
- The easiest way to alter the code to audit a different election is to make sure that csv file containing all the votes is set up in 3 columns with ballot id in the first column, county in the second column, and candidate in the third column. Then the file path just needs to change to read this file.
- Another way to alter the code to audit a different election if the csv file is not set up in the same format, is change which columns the code picks up for the county and candidate.
  * On line 48, change "candidate_name = row[2]" to "candidate_name = row[column index of the candidates]".
  * On line 51, change "county_name = row[1]" to "county_name = row[column index of the candidates]".
- A third way to alter the code to audit a national election is to do a find and replace and change all instances of county to state.
