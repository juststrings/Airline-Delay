
 
 
# Introduction
This is my capstone project submission for Microsoft 30 days of learning with a chosen track of Data analysis using Power Bi.


# Project Name: Airlines Delay Storytelling

![Homejpg](https://user-images.githubusercontent.com/92920156/177653080-fb93b348-cb45-43e6-81f4-b563eb5564c5.jpg)

---
# Problem Objective:   
Story Telling with Power BI
Create a Report that gives the necessary insights on airline delays, the reasons state the given pattern if any and also provides recommendations to avoid delays by airlines in order to maximize their profits and protect their public image



---

# Tools to actualize the project

Power Bi<br>
Excel<br>
Notepad<br>

---
# Data Sourcing

The data was provided by our coach via this links 
theoyinbooke /30Days-of-Learning-Data-Analysis-Using-Power-BI-for-Students
https://raw.githubusercontent.com/theoyinbooke/30Days-of-Learning-Data-Analysis-Using-Power-BI-for-Students/main/Airline%20Project/Airlines.csv

@Theoyinbooke though he gave credit to kaggle.com @ https://www.kaggle.com/datasets/jimschacko/airlines-dataset-to-predict-a-delay

It includes just one table with 9 columns: Id, Airline, Flight, Airport From, Airport to, DaysOfweek, Time, Length and Delay


---

# Data Transformation & Modeling

## Data Transformation

![duplicate](https://user-images.githubusercontent.com/92920156/179702740-c163641b-ac54-408a-a314-d4c3a3b560d7.jpg)


The very first thing I did was to duplicate the original table into 4 new tables and renamed them - flight, destination, Date and Delay respectively.<br>
I did this so I would understand the data better and establish a better relationship. <br>


![flight](https://user-images.githubusercontent.com/92920156/179702981-897bcc4c-09e4-4f10-bcb3-5c809df3b02b.jpg)

In the table named flight. I unpivoted other columns excluding ID, airlines and flights then I removed those unpivoted columns..<br>
I changed the data type of the flight column in the flight table to whole numbers.


![destinations](https://user-images.githubusercontent.com/92920156/179703190-87af8832-108a-45de-be85-3f2edf3ec712.jpg)

Coming down to the table named Destination. <br>
I unpivoted other columns leaving behind ID, Airport from and Airport to.<br>
Then I merged Airport from and Airport to create a column named trip..<br>


![Date](https://user-images.githubusercontent.com/92920156/179703333-dd098f74-026a-4f03-ae44-fd8f0c621b0b.jpg)

In the Date table created, <br>
All other columns were unpivoted then removed aside DaysOfWeek, ID and time 
Then DaysOFweek column data type was changed to Date.<br>
I duplicated the DaysofWeek column thrice.<br>
The first duplicate was renamed day, then I extracted day by the first name from the column.<br>
The second duplicated was renamed Months, I then extracted month by name from the column.<br>
Finally, the last duplicate was renamed Year and then extracted Year from the column.<br>










---
# Findings and Recommendation




---
# Note
File was uploaded as a power BI template due to large size of initial file
