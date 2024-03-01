# PyCity School Analysis #
- PyCity Schools Analysis aims to provide a comprehnsive overview of the school districts performace through various metrics such as the total number of unqiue schools, total number of students, budget, and averages scores. The analysis also gets more indepth into individual schools and analyzing their performances across various metrics such as number of students per school, budget per school, test scores per school, as well as passing rates per school (Math, Reading, and Overall). Finally the analysis examines the relationship between students performance in relation to the grade they are currentley in, school spending, school size, and school type.
---

## Analysis Conclusions
1) The first major conclusion that can be drawn from "PyCity School Analysis" is that the worse that the students at a specific school perform, the more funding / "larger budget" they will have at that school. As show by the "spending_summary" dataframe, you can see that that the far left column is "Spending Ranges (Per Student)" which is increasing from <$585 per student to $645-$680 per student but while "Spending Ranges (Per Studnet)" is increasing, you can also see that in the far right column labeled "% Overall Passing" which is decreasing from 90% of overall student passing both reading and math down to only about 53% of overall students passing reading and math. The logical reasoning for why schools that have worse performance get more funding / "larger budgets" is because the increased budget could help improve learning conditions, hiring better teachers, investing in new technology that makes learning more efficent, or onsite tutors to help more students pass both math and reading in hopes the overall student passing rate increases to a more accetpable rate or atleast get more in-line with the top perfoming schools in the area.

2) Another major conclusion we can draw from "PyCity School Analysis" is that charter schools consitently have better overall test scores for their students compared to district schools. As show by the two dataframes: "top_schools" and "bottom_schools" you can see that the top five BEST performing ("% Overall Passing") schools in "top_schools" dataframe are charter schools with only one of those chater schools having over 2000 students. The top five WORST performing ("% Overall Passing") schools in "bottom_schools" dataframe are all district schools and every single one of those district schools have atleast 2900 students or more attending those schools. The WORST "% Overall Passing" rate for charter schools was 89.23% overall passing rate while the BEST "% Overall Passing" rate for district schools was 54.64% which is still 34.59% away from completing with the WORST charter schools performance. The logical reasoning of why charter schools consitently have better overall test scores for their students compared to district schools is because of less students attending each school allows for better learning conditions and allows students to excel better in their learning journey whether thats through more personalized learning, better teachers, or smaller class sizes for easier comprehension of material.
---

## How Does The Code Work?
1) Import dependecies/libraries for easier functionality of writing Pandas with Python
2) Define and read the two datasets needed for the analysis - "schools_complete.csv" and "students_complete.csv" and then merge the two datasets on "school_name" for a combined dataframe called "school_data_complete"
3) Calculating the total number of unqiue schools, total numbers of students and budget, average math and reading scores, as well as the percentage of math and reading passing rates both individually and combined for an overall passing rate of both math and reading.
4) Creating a dataframe with the calculations above called "district_summary" to display a high_level summary of the DISTRICTS key metrics for schools.
5) Next we want to dive deeper and find metrics per school by finding the school type per school name, students per school, budget per school and budget per student at that respective school, average math and reading scores per school as well as the total number of students that passed reading, total number of students that passed math, and passing both math and reading ==> These math and reading score passing rates are then calculated
6) Then "per_school_summary" dataframe is created based on the calulcations above (described in line 5 in this readme) to created a high_level summary of EACH SCHOOLS specific results
7) "per_school_summary" dataframe then has two columns of values being formatted for easier analysis of numbers "Total School Budget" and "Per Student Budget"
8) Using the "per_school_summary" dataframe ==> the top five BEST performing schools are sorted by "% Overall Passing" and then displayed => Then the same is done for the top five WORST performing schools.
9) Next the "school_data_complete" dataframe is filtered to show results having grades as the column headers grouped by "school_name" to display the average math scores per grade for each school ==> The same exact process is then done for reading scores.
10) Next bins are created for easier analysis => The first bin created was "spending_bins" to create a new column  called "Spending Ranges (Per Student)" in the new a dataframe to categorize spending of each school based on the average test scores and passing rates which is then represented in a new dataframe labeled "spending_summary" and grouped by "Spending Ranges (Per Student)"  ==> The other bin created was "size_bins" to create a new column called "School Size" in the new dataframe to figure out the sizes of each school and then the averages of the tests scores and passing rates are caulcated and grouped by " School Size" in a new dataframe labeled "size_summary"
11) Finally average test scores are calculated as well as the passing rates and are then grouped by "School Type" to show a high_level summary of average math and reading test scores as well as passing rates of math, reading, and both based on "School Types" (District or Charter).
12) Draw conclusions from the analysis
   
