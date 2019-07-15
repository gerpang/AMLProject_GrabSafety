## Data Prep Steps
As performed in `1DataPrep.ipynb`. 
0.  Load data from separate files and append to form 1 main file. 
1.	Remove Duplicate labels
2.	Remove Inaccurate records, i.e.:
    - second >= 10000 (more than 2 hours long trip, unlikely in SG. Drill down also shows that these high numbers are not continuous with their preceding 'correct' records.)
    - Speed < 0 (physically impossible)
3. Remove Inaccurate trips, i.e.:
    - Trips where the % of data collected/entire known duration of the trip (highest recorded `second`) is > 90%. 
    - Only some records at the end of the trip which are negative – the rest are correct. (Number of records = Max(second)) 
4.	Missing Records Imputation
    - Some bookingIDs have missing records, including those we have removed earlier for being inaccurate. 
    - We will use rolling window to impute these missing records *only* if the gap between records is not more than 5 seconds. 