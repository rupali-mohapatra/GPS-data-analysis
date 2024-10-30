# mobility-data
The purpose of this assignment is to perform the quality and processing of mobility data.
Mobility data is one of the data collection methods used to find human mobility patterns,
urban mobility models, transportations studies, etc. In this lab, you will learn to process the
raw GPS data. The quality of data depends on the source of data, which needs to be evaluated.
You will learn to clean and process GPS data. Task 1 is changing the format file to the proper
version, while task 2 aims to clean and process the data
Task1:
1. Download the dataset named raw data.
2. Import the dataset in Excel (Import as a text)
[Date] (This is the Date when the data was transferred from the GPS logger to the computer.)
[TP] (This means how many tips are done during the period, but this information is not very
useful, because it just had the Date and the starting time)
[001, 2011-04-15:07:51:03]
Below this line is the information about the recording points.
For example: 1=60267285,15286898,55103,150411,100,-1
From left to right after the = sign, it is: Latitude, Longitude, time, Date, speed, and altitude
However, they are not in the right format.
The format of the original recording for the coordinates is not in decimal degree, but in decimal degree
minutes.
For example, in the original .gsd file, the original one is 60267285, which the true format is 60
(degree)26.7285(decimal minutes)
If we want to change it to decimal degree, we need to divide the decimal minutes part by 60 to get the
decimal degree part
Therefore it should be:
60 + (26.7285/60) Which means, to get the WGS84 decimal degree, you need to conduct calculation:
60267285 -> 60+ (26.7285/60)
15286898 -> 15+ (28.6898/60)
55103 -> 05:51:03
150411 -> 15-04-2011
100 -> 100/100 =1 km/h (this speed column should all divide 100)
-1 -> no recording for altitude, note by -1
You can decide the format for time and Date, but Y, X and Speed, you should follow exactly the
calculation. Each recording should have its own id. Find your own way to preprocess the data and
save the data in a CSV or XLSX file.
3. Create a Trip ID and Point ID based on the data.
4. Calculate the speed based on km/h.
5. Change the Time and Date in a proper version.
6. Calculate the distance between two points.
7. Calculate the time difference between two points.
8. Calculate the average speed on the trip.
9. Calculate the acceleration at each point.
10. Calculate average acceleration on the trip.
11. Calculate the trip duration and distance.
Task2:
Visualization the data
1- Visual the data in python, R or any relevant software (longitude vs latitude).
2- Generate a heatmap to show the density of GPS data points in a specific area.
