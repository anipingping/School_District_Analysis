# School District Analysis
## Overview
### This report was prepared for the Chief Data Scientist of the city school district. The analysis assessed the nature and quality of student-specific and school-specific data including student names, student math and reading scores, school budget, school budget per student and the school type (charter or district school). The purpose of this report is to yield some insight into comparative school performance, cost effectiveness and other per-student measures of quality. The data for Thomas High School was determined to be of questionable honesty. It was asserted at the beginning that Thomas HS 9th graders' reading and math scores were unreliable, so I made a partially successful effort to recalibrate the data for better accuracy.
## Results
### District Summary
#### As shown in the table below there are a total of 15 schools comprised of just under 40,000 students. The district's budget is approximately $24.6 million. A range of district-wide average math and reading scores are also available. 
![District_Summary](https://user-images.githubusercontent.com/106618404/179428978-001e284d-d99c-4999-a66f-014d973ef0b3.PNG)

#### The table below lists schools by type. There are 8 charter schools, 7 district schools.
![Schools_by_type](https://user-images.githubusercontent.com/106618404/179439275-a31874d3-b075-44bd-b4c0-9ecdb86598d0.PNG)

### School Summary
The School Summary table below shows total school budget, per student budget, average math and reading scores per student and the percentage of students passing each subject. The last column bins each school into a spending per student category. In the original analysis, the top 5 schools in these data are: Cabrera, Griffin, Wlison, Pena and Wright High School.
![Top_5_schools_original](https://user-images.githubusercontent.com/106618404/179432635-929cb1a0-05f0-4eaa-9eea-566bad212cc6.PNG)

The table below groups the schools into small, medium, and large size categories with each group's average math and reading scores as well as each group's passing percentages in each category. This table seems to indicate that small schools perform somewhat better.
![School_performance_by_size](https://user-images.githubusercontent.com/106618404/179439589-7453370e-8477-4302-9122-71aa81a24e26.PNG)

There was a question, however, about the legimitacy of 9th grade reading and math scores at Thomas High School. Accordingly, my code removes 9th grade reading and math scores, replaces the scores with null values, and re-calculates Thomas HS metrics without the invalid figures. You can see values for certain students have been removed and replaced by the letters "NaN" or "Not a Number" and are thereby removed from the analysis (see table below):
![Thomas_HS_Null_Values](https://user-images.githubusercontent.com/106618404/179429913-c760b320-9f7d-4361-8ea8-d3b20f072f35.PNG)

Correcting for the 9th grade students that were determined to have invalid test scores and using only 10th-12th grade students, Thomas HS overall passing percentage moves it into the top 5 schools in the district.

![School_Summary](https://user-images.githubusercontent.com/106618404/179429665-8c64a360-c0a6-4427-842a-6aa92e21e442.PNG)
![Thomas_HS_Summary](https://user-images.githubusercontent.com/106618404/179429822-91305cc7-e7c9-4fd8-9e3d-737a77aaff68.PNG)

### How each school was affected by the changes in the data
Thomas HS performance metrics was substantially altered by a correction for the 9th grade scores that were filetered out of this data. Thomas HS performance metrics like overall passing % initially fell dramatically, but with coding that corrects for the students who are missing test scores, the percentages actually increase above their original, false figures. The other schools that were around 90 percent overall passing lost their rankings by one spot as Thomas HS overall percentage of 90.63 is sufficiently high to place it in 2nd on the original chart -- a greater overall passing percentage than Wright, Wilson, Pena, and Griffin (according to the original data). With updated code that looks at 10th-12th grade only, Thomas HS would replace Wright HS in the rankings of overall passing percentages.

## Summary 
### 4 changes to the school district analysis

1. Thomas HS overall passing percentage drops significantly when test scores from 9th grade are dropped from the analysis.
2. When only 10th-12th grade test scores are assessed, Thomas HS overall passing percentages increase significantly, placing Thomas in the Top 5 overall passing percentages.
3. Other schools, particularly Wright HS, are impacted by Thomas HS ranking. Wright HS drops out of the Top 5
4. A final significant change is to think about the impacts on the overall dataset if removing/adjusting the scores of one class in one school (Thomas) can have such a drastic impact on rankings and potential funding considerations. The quality and legitimacy of the other schools' data probably needs to be verified before any final decisions can be made that assign dollars to schools based on their reported performance. My recommendation based on this study is to require the schools to report a second time, compare that entire dataset against this dataset, and run this report again for due diligence. 
