# surfs_up
 Run Anlaytics on weather dataset for Oahu island using SQLite, SQLAlchemy, and Flask.

## Overview of the statistical analysis:
While on vacation to Hawaii last year we have been trying to come up with a plan that will let us just return to Hawaii but live there forever. A Surf n' Shake shop serving surfboards and ice creams to locals, tourists and of course us seems like a good idea. We have some saving we're willing to invest but we'll need some real investor backing to get this  off the ground.

W. Avy is an investor who is an avid surfer and likes our idea. But, he wants more information about temperature trends before opening the surf shop. Specifically, he wants temperature data for the months of June and December in Oahu, in order to determine if the surf and ice cream shop business is sustainable year-round.

## Resources
* Data Source: [Oahu_Weather_details sqlite](https://github.com/sucharita1/surfs_up/blob/32665b9d431365df56dd64602ec665b0ce3ae0cb/hawaii.sqlite)
* Software: Python 3.7.10, Jupyter notebook 6.3.0

## Results:
The results as seen from [SurfsUp_Challenge.ipynb](https://github.com/sucharita1/surfs_up/blob/8b8d76769730e6394c97a3eec8dec9b3082ccefa/SurfsUp_Challenge.ipynb) jupyter notebook of the temperature data for the month of June and December show the following differences:
1. There are 1700 records for the month of June while only 1517 records for the month of december. Maybe one of the stations was closed during the month of december or there was some issue on certain dates or at certain stations. 

![Jun_tobs](https://github.com/sucharita1/surfs_up/blob/32665b9d431365df56dd64602ec665b0ce3ae0cb/Resources/Jun_tobs.png?raw=true)
June Tempertaure Statistics 

![Dec_tobs](https://github.com/sucharita1/surfs_up/blob/32665b9d431365df56dd64602ec665b0ce3ae0cb/Resources/Dec_tobs.png?raw=true)
December Temperature Statistics

2.  June will be a little hotter at 75 degrees mean temperature. While minimum temperature of June is 64 degrees but most of the time it will be much hotter than that as the least 25% of the days the temperture will be around 73 degrees. Rest of the days it will be hotter with max at 85. The standard deviation is almost the same at 3.26 for June.  The median is also the same as mean which means results are not skewed.
![Jun_temp](https://github.com/sucharita1/surfs_up/blob/32665b9d431365df56dd64602ec665b0ce3ae0cb/Resources/Jun_temp.png?raw=true)

3. For the month of december the  mean temperature is 4 degrees less. That means december will be much cooler at 71 degees and the weather will be pleasant. The minimum temperature for the month of december is 56 degrees and for 25% or 1/4 th of the days the temperature will remain at or below 69 degrees. The standard deviation is almost the same at 3.75 for december. The median is also the same as mean which means results are not skewed.
![Dec_temp](https://github.com/sucharita1/surfs_up/blob/32665b9d431365df56dd64602ec665b0ce3ae0cb/Resources/Dec_temp.png?raw=true)


## Summary:
The weather during the months of June and December can be summarized as follows:
* The weather results of Oahu Beach tell us that the temperatures follow a symmetrical pattern and tempertaures are neither skewed to the colder side nor the hotter side. 

We have already seen maximum, minimum, mean, median and 1st and 2nd quartiles for June and December temperture at various stations over the years. 
But, if we get data in terms of days by observing the data from a single station for a particular June and December we can make better decisions.

* We will get a better idea of June and December weather in term of days if we check out the most active station that i.e. USC00519281 , and see the data for the month of June 2016 and December 2016. We will get even more information by drawing a histogram. 
![June_Query.png](https://github.com/sucharita1/surfs_up/blob/32665b9d431365df56dd64602ec665b0ce3ae0cb/Resources/June_Query.png?raw=true)
![Dec_Query.png](https://github.com/sucharita1/surfs_up/blob/32665b9d431365df56dd64602ec665b0ce3ae0cb/Resources/Dec_Query.png?raw=true)

We can see from the histogram that temperature at USC00519281 station in Oahu was more than 67 degrees for 28 days in December and 29 days in June

* We can also query to find out the days when the temperture was optimal i.e. between 72 degrees and 83 degrees in June and December:
![Most_comfortable_June.png](https://github.com/sucharita1/surfs_up/blob/32665b9d431365df56dd64602ec665b0ce3ae0cb/Resources/Most_comfortable_June.png?raw=true)
![Most_comfortable_Dec.png](https://github.com/sucharita1/surfs_up/blob/32665b9d431365df56dd64602ec665b0ce3ae0cb/Resources/Most_comfortable_Dec.png?raw=true)

We can see that the weather was most comfortable i.e. between 72 degrees and 83 degrees in June for 22 days and in December for 12 days.

Finally , we can see that temperatures are quiet reliable and predictable in Oahu even December month has some good days. Looks like a Surf n' Shake shop might be soon on the cards.


