# PyCity Schools
An analysis of school district test data.

## Overview
My client, a city school district, asked me to analyze reading and math test results for all the students in the district's 15 schools. I was instructed to create a list of the highest performing schools as well as the lowest performing schools and tasked with uncovering possible trends such as how school funding, size and type affect test performance. The results of my analyses would guide the district's decisions with regard to funding and priorities.

I used Python's Pandas library to clean the data and create data frames to analyze it.

My initial findings were as follows.
* Charter schools outperformed district schools.
* Small (fewer than 1,000 students) and medium (1,000 - 2,000 students) schools performed better than large (2,000 - 5,000 students).
* Schools with lower spending per student performed better than those with higher spending.
  + This may have been because charter schools tend to have a lower spending per student.
* The top performing schools were (in order) Cabrera High School, Thomas High School, Griffin High School, Wilson High School and Pena High School -- all charter schools.
* The lowest performing schools were Johnson High School, Hernandez High School, Huang High School, Figueroa High School and Rodriguez High School.

Though pleased with my initial analysis, my client contacted me again to notify me of suspected academic dishonesty in 9th grade test scores from Thomas High School (THS), a charter school with a per-student budget of $638. I was to perform the analysis again after factoring out THS 9th graders. Using Python's Pandas library I was able to replace the THS 9th graders' scores with null values that would not be factored into calculations. I then used Pandas to analyze the data by creating data frames. 

## Results of Second Analysis
After running the analysis on the district schools excluding THS 9th graders, I compared data frames from the first and second analysis side by side. These were the results.

* I was most interested in how Thomas High School's position in the list of top schools would be affected.

Here is a screenshot of the data frame from the first analysis displaying the top schools.
![first analysis top schools](https://github.com/LiShanDa2021/school_district_analysis/blob/main/resources/old%20top%20schools.png?raw=true)

And here are the top schools from the second analysis.
![second analysis top schools](https://github.com/LiShanDa2021/school_district_analysis/blob/main/resources/new%20top%20schools.png?raw=true)

As you can see, the scores including the 9th graders are indeed higher, but not enough to affect THS's position among the top schools. In fact, in order to see any difference, I had to display the data frames without formatiing the data. The scores would not have rounded differently.

* Since removing 9th graders seemed to only have a small effect on THS's raw scores and position among top schools, I was doubtful it would have any effect at the district level. The effect was indeed small, though it may be meaningful. I have presented the results without formatting them because that is the only way to detect the difference.

First district summary:
![first district summary](https://github.com/LiShanDa2021/school_district_analysis/blob/main/resources/old%20district%20summary%20not%20rounded.png?raw=true)

Second district summary:
![second district summary](https://github.com/LiShanDa2021/school_district_analysis/blob/main/new%20district%20summary%20not%20rounded.png?raw=true)

In the first district summary, the percent of students passing both tests was just over 65%, in the second summary it is just under. It is a small difference, but it just may be significant when it comes to funding. After all, at 64, we round down to 60 and at 65 we round up to 70.

* I next looked at whether or not removing THS 9th graders would have much effect on 9th graders' performance district wide.

Here is a screenshot of the first analysis of 9th grade scores districtwide.

![old 9th grade scores](https://github.com/LiShanDa2021/school_district_analysis/blob/main/old%209th%20grade%20scores.png?raw=true)

And here is a screenshot of the second analysis.

![new 9th grade scores](https://github.com/LiShanDa2021/school_district_analysis/blob/main/new%209th%20grade%20scores.png)

While the scores with THS 9th graders factored out are indeed lower, they are only lower by a fraction of a percent.

* I then looked at whether or not removing THS 9th graders would affect school performance by spending bracket. Note that THS is in the $630-644 spending bracket.

These are the scores by spending bracket including THS 9th graders.

![first analysis scores by spending](https://github.com/LiShanDa2021/school_district_analysis/blob/main/resources/old%20school%20spending%20ranges.png?raw=true)

And these are the scores by spending excluding the THS 9th graders.

![second analysis scores by spending](https://github.com/LiShanDa2021/school_district_analysis/blob/main/resources/new%20school%20spending%20ranges.png?raw=true)

Scores by school size
Scores by school type


## Summary
As THS 9th grade students make up only 1.2% of the district population (461 out of a student population of 39170), my hypothesis was that the effects of removing their scores would be small. 

inconclusive
warrants further investigation

461 out of 39170
mere 1.2%

Summary: Summarize four changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs.
