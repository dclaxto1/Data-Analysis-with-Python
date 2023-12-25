# Data-Analysis-with-Python
Performed the necessary calculations and then create a high-level snapshot of the district's key metrics in a Pandas DataFrame. <br />
Including the following:<br />
Total number of unique schools: **15**<br />
Total students: **39,170**<br />
Total budget: **2469428**<br />
Average math score: **78.99**<br />
Average reading score: **81.88**<br />
% passing math (the percentage of students who passed math): **74.98** <br />
% passing reading (the percentage of students who passed reading): **85.81**<br />
% overall passing (the percentage of students who passed math AND reading): **65.17**<br />
![image](https://github.com/dclaxto1/Data-Analysis-with-Python/assets/128431134/8aa9c6b4-0afc-4927-9505-8a271ac39a8a)


## School Summary<br />
Performed the necessary calculations and then create a DataFrame that summarizes key metrics about each school.

Included the following:<br />
School name: **14 differ3ent school names**<br />
School type: **2**<br />
Total students: **39,170**<br />
Total school budget: **2469428**<br />
Per student budget:<br />
![image](https://github.com/dclaxto1/Data-Analysis-with-Python/assets/128431134/843e09d0-ec48-4feb-957d-785bf57bec5b)

Average math score<br />
Average reading score<br />
![image](https://github.com/dclaxto1/Data-Analysis-with-Python/assets/128431134/ecb42434-003a-4c27-8ecc-5ec12280c69b)

% passing math (the percentage of students who passed math)<br />
![image](https://github.com/dclaxto1/Data-Analysis-with-Python/assets/128431134/3d1a3d95-5b23-4b78-99b4-4aa7769183d4)

% passing reading (the percentage of students who passed reading)<br />
![image](https://github.com/dclaxto1/Data-Analysis-with-Python/assets/128431134/446f5326-62fa-454d-b02f-0693d8f3d932)

% overall passing (the percentage of students who passed math AND reading)<br />
![image](https://github.com/dclaxto1/Data-Analysis-with-Python/assets/128431134/bdbd0ffa-73d3-4138-9a93-2920c44d4524)

## Highest-Performing Schools (by % Overall Passing)<br />
Sorted the schools by % Overall Passing in descending order and display the top 5 rows.<br />

Saved the results in a DataFrame called "top_schools".<br />
<br />
Lowest-Performing Schools (by % Overall Passing)<br />
Sorted the schools by % Overall Passing in ascending order and display the top 5 rows.<br />

Saved the results in a DataFrame called "bottom_schools".<br />

Math Scores by Grade<br />
Performed the necessary calculations to create a DataFrame that lists the average math score for students of each grade level (9th, 10th, 11th, 12th) at each school.<br />

Reading Scores by Grade<br />
Created a DataFrame that lists the average reading score for students of each grade level (9th, 10th, 11th, 12th) at each school.<br />

Scores by School Spending<br />
Created a table that breaks down school performance based on average spending ranges (per student).<br />

Used the code provided below to create four bins with reasonable cutoff values to group school spending.<br />

spending_bins = [0, 585, 630, 645, 680]<br />
labels = ["<$585", "$585-630", "$630-645", "$645-680"]<br />
Use pd.cut to categorize spending based on the bins.<br />

Used the following code to then calculate mean scores per spending range.<br />

spending_math_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"])["Average Math Score"].mean()<br />
spending_reading_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"])["Average Reading Score"].mean()<br />
spending_passing_math = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Passing Math"].mean()<br />
spending_passing_reading = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Passing Reading"].mean()<br />
overall_passing_spending = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Overall Passing"].mean()<br />
Use the scores above to create a DataFrame called spending_summary.<br />

Included the following metrics in the table:<br />
Average math score<br />
Average reading score<br />
% passing math (the percentage of students who passed math)<br />
% passing reading (the percentage of students who passed reading)<br />
% overall passing (the percentage of students who passed math AND reading)<br />
Scores by School Size<br />
Use the following code to bin the per_school_summary.<br />
size_bins = [0, 1000, 2000, 5000]<br />
labels = ["Small (<1000)", "Medium (1000-2000)", "Large (2000-5000)"]<br />
Use pd.cut on the "Total Students" column of the per_school_summary DataFrame.<br />
Create a DataFrame called size_summary that breaks down school performance based on school size (small, medium, or large).<br />
Scores by School Type<br />
Use the per_school_summary DataFrame from the previous step to create a new DataFrame called type_summary.<br />

This new DataFrame showed school performance based on the "School Type".<br />
