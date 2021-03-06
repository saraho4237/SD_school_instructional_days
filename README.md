# EDA and Visualizations from South Dakota School District Data

### Why look at this Data?

It all started with some Facebook chirping:

![](images/i1.png)

Followed by...

![](images/i2.png)

It got me thinking, 1) there has to be data on this, and 2) there has to be a cool way to visualize the data to see what's what when it comes to schools with a 4 day week.

Further, I wanted to see what kind of data South Dakota was keeping on its schools.

### District Level Data

The data is from the [South Dakota Department of Education Data Center](https://doe.sd.gov/data.aspx) and includes district level information from the 149 public school districts in South Dakota. The columns included in the final dataset were ones I pulled based on what I thought might be interesting.

The cleaned/merged dataset includes information on:
* District Name
* Location
* County
* County Population
* K-12 Enrollment Fall 2017
* Dropout Rate
* Attendance Rate
* Free & Reduced Lunch Eligibility Percentage
* Percent of Special Education Students
* Average Teacher Salary
* Average Teacher Years of Experience
* Percentage of Teachers with Advanced Degrees,
* Average ACT Composite Score
* Number of Students Taking the ACT
* Average Number of Instructional Days
* Average Number Instructional Hours
* 4 Day School Week (yes/no)

*To compute instructional hours and days for each district, the average numbers of hours and days were taken from each of the schools in the district.*

*Additionally, if over 50% of schools in the district implemented a 4 day week, the district was counted as having a 4 day week, overall.*

Unfortunately, the data does **not** include information on schools overseen by the Bureau of Indian Education (BIE). Data on BIE schools proved difficult to find in a tabular format/.csv. The BIE provides a link to a report card for many of its schools. The latest reports are from the 2015-2016 school year (ex. [Saint Francis Indian School](https://www.bie.edu/cs/groups/xbie/documents/text/idc2-074499.pdf)).

### Missing Data

The dataset has complete information for all columns except:

* Free & Reduced Lunch Eligibility Percentage
* Percent of Special Education Students
* ACT Composite Score

11 districts did not report their free and reduced lunch percentage.

Elk Mountain School District was the only district to not report their special education percentage.

41 did not report an average ACT composite score. All districts that did not report a composite score had fewer than 10 students take the ACT. Two districts had no students take the ACT: Big Stone City School District and Elk Mountain School District.

### Tableau Public Visualization

Check out the interactive visualization I made from this data [here.](https://public.tableau.com/profile/sarah.o.neil#!/vizhome/SDSchoolDistrict-LevelDataDashboard/Dashboard12)

The visualization hones in on the county population and free/reduced lunch data for 4- vs. 5-day school districts.

I chose these to focus on these because the FB comments above were interested in exploring whether rural districts were more likely to be 4-day and whether schools with more students of color were more/less likely to be 4-day.

I used county population and free/reduced lunch rate as proxy variables to indicate rural-ness and racial/ethnic breakdown respectively.

**The visualizations show the median county population is actually slightly higher for districts that have a 4-day school week.** I used median for measure of center because the population data was right skewed.

Additionally, **schools with a 4-day week had a slightly higher average percentage of students who qualify for free/reduced lunch** (.384 for 4-day districts vs .339 for 5-day districts).

## More Visualizations

If you are interested in how school districts with 4- vs. 5-day weeks differ on other metrics, [check this out](https://public.tableau.com/profile/sarah.o.neil#!/vizhome/SDSchoolDistrict-LevelDatastory/Story1). I include metrics related to teacher pay, ACT score, instructional time, etc.  

You might notice, there are some possible data entry errors. For example, Hoven School District...303 instructional days. Doubtful. If I was doing formal analyses, I would have removed these questionable data points. However, this is simply a visualization exercise.

To address one final comment, an FB poster mentioned that low SES students tend to go to school longer than their higher SES counterparts.

This does not appear to be the trend in SD:

![](images/corr.png)

### A few final thoughts on the public data...

South Dakota could do a much cleaner job of reporting district race/ethnicity information. It is obviously not ideal to use free/reduced lunch status as a proxy for race/ethnicity (though race and socioeconomic status are, more often than not, highly correlated).

It would also be great if the data included information on whether or not the school is located on reservation/tribal lands.

The South Dakota Department of Education could do a much better job of documenting their datasets by including metadata on what information is included in each of their many tables. For example, the columns "Capital Outlay Fund Local Revenue" and "Special Education Extraordinary Cost Funds"... what do these mean?? There are close to 100 of these "hard-to-interpret-unless-you-are-a-CPA" columns related to district funding. But zero easily accessible columns relating to race/ethnicity. IDK.

Finally, the BIE should be more transparent with their data (i.e. publish their data on the BIE website in a tabular format as the department of education seems mandated to do). I suppose there could be funding/other barriers that keep the BIE from keeping tabluar public data.
