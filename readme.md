# Grab AI challenge 
Started on 11th June 2019
Due 17th June 2019, 6.00pm SGT. 

## About the Challenge 
Based on telematics data, how might we detect if a driver is driving dangerously?
Given the telematics data for each trip and the label if the trip is tagged as dangerous driving, derive a model that can detect dangerous driving trips.

## Pre-Requisite Downloads 
#### Safety Dataset 
Information about the challenge and the dataset can be found from (Grab AI website)[https://www.aiforsea.com/safety]

## Features 
### Acceleration and Gyroscope Readings
Cases: 
- Box is not moving: (X,Y,Z) = (0,0,-1). 
- 
Gyroscopep is less sensitive to linear mechanical movements, and is used to smooth out any acceleration errors. We might want to average both accelerometer and gyroscope data to better estimate current device cinclination. 

A proposed algorithm by Starlino electronics is used to determine the 'best bet' of the current device's position. [2](http://www.starlino.com/imu_guide.html)


### Driver Profiling 
We might be interested to look at how to identify dangerous **drivers** rather than just dangerous trips. If a driver tends to drive dangerously more often, this is more risky than a driver who only drove dangerously once. However the data is anonymized and we cannot tell which bookingID was completed by which driver. We might want to develop an algorithmic signature of driving type (driver profiling based on a telematic fingerprint).