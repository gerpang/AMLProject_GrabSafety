# Cleaning Steps
## Grab Safety Data 

1.	Remove Duplicate labels
2.	Remove raw records where second >= 10000 (more than 2 hours long trip)
    - Only some records at the end of the trip which are negative – the rest are correct. (Number of records = Max(second)) 
    - Records removed by this rule:  
3.	If speed suddenly dips to -1 and the x records before/after it are normal (high), use moving average to impute.
    - Some bookingIDs have majority of records with Speed < 0
