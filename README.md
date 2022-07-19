
 
 
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

### 1.
![duplicate](https://user-images.githubusercontent.com/92920156/179702740-c163641b-ac54-408a-a314-d4c3a3b560d7.jpg)


The very first thing I did was to duplicate the original table into 4 new tables and renamed them - flight, destination, Date and Delay respectively.<br>
I did this so I would understand the data better and establish a better relationship. <br>

### 2.
![flight](https://user-images.githubusercontent.com/92920156/179702981-897bcc4c-09e4-4f10-bcb3-5c809df3b02b.jpg)

In the table named flight. I unpivoted other columns excluding ID, airlines and flights then I removed those unpivoted columns..<br>
I changed the data type of the flight column in the flight table to whole numbers.

### 3.
![destinations](https://user-images.githubusercontent.com/92920156/179703190-87af8832-108a-45de-be85-3f2edf3ec712.jpg)

Coming down to the table named Destination. <br>
I unpivoted other columns leaving behind ID, Airport from and Airport to.<br>
Then I merged Airport from and Airport to create a column named trip..<br>

### 4.
![Date](https://user-images.githubusercontent.com/92920156/179703333-dd098f74-026a-4f03-ae44-fd8f0c621b0b.jpg)

In the Date table created, <br>
All other columns were unpivoted then removed aside DaysOfWeek, ID and time 
Then DaysOFweek column data type was changed to Date.<br>
I duplicated the DaysofWeek column thrice.<br>
The first duplicate was renamed day, then I extracted day by the first name from the column.<br>
The second duplicated was renamed Months, I then extracted month by name from the column.<br>
Finally, the last duplicate was renamed Year and then I extracted Year from the column.<br>


### 5.
![Delay](https://user-images.githubusercontent.com/92920156/179704129-404a99d3-cace-4b94-ba2f-42af6f687114.jpg)

The last table was created by duplicating the airline table which was named delay.<br>
I unpivoted other columns and then deleted them aside. ID, Time, length and Delay<br>
Then I changed the data type of bother length and Delay to whole numbers.<br>



## Data Model

![model](https://user-images.githubusercontent.com/92920156/179704928-a132b883-63e5-4b9d-84be-93731c79d634.jpg)

In the modelling section, I used the ID as the key for all tables and then used it to connect all the tables to a fact table which was the airline table.

---

# Findings and Recommendation

### Note: 

I positioned myself as a data analyst for the airline with the highest delay in order to understand the data better.
You might ask why choosing an airline with the
Highest delay I did that in other to understand the data better and I also believe the airline with the highest delay requires more attention so they would be able to reduce their delay (I e protecting their public image and relationship with customers) and also balance their profit


### Now let's dive into my findings.

Taking insights from the bookmarked top 5 section of the reports which consist of the top 5 airlines in terms of flight, delay and length

![top 5](https://user-images.githubusercontent.com/92920156/179706456-9937055c-35b7-45ec-932d-e11a56b1be34.jpg)

#### Scenario One for Top 5 Section

* When comparing airline WN with airline OO, you would notice that despite the fact that OO has more flights travelled compared to WN. Airline OO happens to be the third airline in terms of delay.<br>
What is the cause of this you may ask? This is due to no other fact that airline WN has a reasonably high distance travelled compared to OO with a corresponding relatively high flight covered though less than OO. <br>
Meaning that LONGER LENGTH TRAVELLED LEADS TO A HIGHER CHANCE OF DELAY

* Looking at the relationship between Airline DL and Airline MQ.<br>
It will be seen that this relationship is re-establishing the relationship between Airlines WN and OO. <br>
That's a longer distance travelled by airline DL to that of airline MQ but a smaller flight covered by Airline DL to Airline MQ leads to a higher delay by airline DL than that airline MQ







---
# Note
File was uploaded as a power BI template due to large size of initial file
