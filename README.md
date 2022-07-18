# School District Analysis
## Overview
### This report was prepared for the Chief Data Scientist of the city school district. The analysis assessed the nature and quality of student-specific and school-specific data including student names, student math and reading scores, school budget, school budget per student and the school type (charter or district school). This report yields some insight into school performance, cost effectiveness and comparative performance. The data for Thomas High School was determined to be of questionable honesty so I made a partially successful effort to recalibrate the data for better accuracy.
## Results
### District Summary
As shown in the table below there are 15 total schools comprised of just under 40,000 total students. The district's total budget is approximately $24.6 million. A range of average math and reading scores are also available. 
![District_Summary](https://user-images.githubusercontent.com/106618404/179428978-001e284d-d99c-4999-a66f-014d973ef0b3.PNG)

### School Summary
The School Summary table below shows total school budget, per student budget, average math and reading scores per student and the percentage of students passing each subject. The last column bins each school into a spending per student category. In the original analysis, the top 5 schools in these data are: Cabrera, Griffin, Wlison, Pena and Wright High School.
![Top_5_schools_original](https://user-images.githubusercontent.com/106618404/179432635-929cb1a0-05f0-4eaa-9eea-566bad212cc6.PNG)

There was a question, however, about the legimitacy of 9th grade reading and math scores at Thomas High School. Accordingly, my code removes 9th grade reading and math scores, replaces the scores with null values, and re-calculates Thomas HS metrics without the invalid figures. You can see values for certain students have been removed and replaced by the letters "NaN" or "Not a Number" and are thereby removed from the analysis (see table below):
![Thomas_HS_Null_Values](https://user-images.githubusercontent.com/106618404/179429913-c760b320-9f7d-4361-8ea8-d3b20f072f35.PNG)

Correcting for the 9th grade students that were determined to have invalid test scores and using only 10th-12th grade students, Thomas HS overall passing percentage moves it into the top 5 schools in the district.

![School_Summary](https://user-images.githubusercontent.com/106618404/179429665-8c64a360-c0a6-4427-842a-6aa92e21e442.PNG)
![Thomas_HS_Summary](https://user-images.githubusercontent.com/106618404/179429822-91305cc7-e7c9-4fd8-9e3d-737a77aaff68.PNG)

### How each school was affected by the changes in the data (10 pt)
Thomas HS performance metrics was substantially altered by a correction for the 9th grade scores that were filetered out of this data. Thomas HS performance metrics like overall passing % initially fell dramatically, but with coding that corrects for the students who are missing test scores, the percentages actually increase above their original, false figures. The other schools that were around 90 percent overall passing lost their rankings by one spot as Thomas HS overall percentage of 90.63 is sufficiently high to place it in 2nd on the original chart -- a greater overall passing percentage than Wright, Wilson, Pena, and Griffin (according to the original data).

## Summary - there is a statement summarizing four changes to the school district analysis after reading and math scores have been replaced (5 pt)
