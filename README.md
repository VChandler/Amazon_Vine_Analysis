# Amazon Vine Analysis
## Overview  
The project's goal is to analyze Amazon reviews and compare Amazon Vine vs. non-Vine results to see if there is any bias toward favorable reviews.  In this case, the dataset comes from Amazon and focuses on video games.  
For this project, PySpark was used to perform the ETL process.  It was subsequently loaded into an Amazon RDS instance, and analyzed using Pandas.  
## Results  
For both datasets, we only examined data where:
* Total votes was greater or equal to 20, AND
* The percentage of helpful votes was at least 50% of the products' reviews  

### Non-Vine Program  
We first examined the dataset for non-Vine program reviews:  

![non_vine](https://user-images.githubusercontent.com/88070999/144356646-34bc6f71-71bf-4e97-a6c5-5be44af9b570.png)  
As seen from the Pandas output, there are three key numbers:  
* 40,471 total reviews
* 15,663 five star reviews
* 39% of the total reviews were rated as five stars  

### Vine Program  
We next examined the dataset for Vine program reviews:

![vine_summary](https://user-images.githubusercontent.com/88070999/144356674-b8490b12-7e5b-49ea-9562-2837c5809b98.png)  

For this set of data, the three key numbers:  
* 94 total reviews
* 48 five star reviews
* 51% of the total reviews were rated as five stars  

## Summary
The number of Vine reviews was a fraction of the size of the non-Vine reviews.  That aside, there does appear to be a bias towards five star reviews for those users participating in the Vine program (a full 12 percentage points higher for the Vine program vs. the non-Vine reviews).

### Further Analysis  
For futher analysis, it may be beneficial to find other Amazon datasets that have a much higher number of Vine-participant reviews.  This would enable a larger sample size and potentially less of a standard deviation, making the results more reliable.  I would also recommend statistical tests such as a t-test to take a more rigorous look as to whether the difference between the two groups are statistically significant.
