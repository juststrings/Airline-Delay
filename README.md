
 
 
# Introduction
This is my submission for Microsoft 30 days of learning capstone project with a chosen track of Data analysis using Power Bi.


# Project Name: Airlines Delay Storytelling

![Dashboard](https://user-images.githubusercontent.com/92920156/179711859-5a93a144-3147-4ff6-a3f0-b2aff760d567.jpg)


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

The data includes just one table with 9 columns: Id, Airline, Flight, Airport From, Airport to, DaysOfweek, Time, Length and Delay


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
Highest delay I did that in other to understand the data better and I also believe the airline with the highest delay requires more attention so they would be able to reduce the factors causing their delay in order to protect their public image and relationship with customers and also balance their profit


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

### Scenario Two for Top 5 Section

* Looking at the relationship between Airlines US and UA.<br>
You would notice that airline US has a shorter distance travelled compared to that of airline UA.<br>
Though, Airline US has a longer flight covered than Airline UA.<br>
This led to a higher delay by airline US than airline UA because their difference in length it's quite small unlike their huge difference in flight which gave airline US a higher delay.<br>
That is LONGER FLIGHT LEADS TO A HIGHER CHANCE OF DELAY if the difference between the length/distance travelled are close. <br> <br>


Taking insights from the bookmarked bottom 5 section of the reports which consist of the bottom 5 airlines in terms of flight, delay and length.

![bottom 5](https://user-images.githubusercontent.com/92920156/179707977-b188012f-cd57-417f-9e80-7d8dcf2ea15d.jpg)

* When looking at the relationship between OH and AS.<br>
One will notice that OH has a far higher flight covered than AS but a lower delay compared to AS. 
One would have expected airline OH to have the most delay due to its huge flight covered compared to airline AS minute flight covered in respect to airline OH but airline OH's slightly lesser distance/length travelled is a disadvantage with other untold circumstances not given or covered by this data such as weather. <br>
However, this is re-establishing the fact that Length travelled has precedence over flight covered in terms of delay.

* Analysis Airline YV, F9 and HA <br>
Nothing really special between the relationship between YV, F9 AND HA because the flight covered by YV is the highest with F9 being higher and HA the lowest. Same when looking at their relationship in terms of length. Therefore this leads to YV having the highest delay and HA having the lowest delay. <br>
Restating the fact of length is an important factor to consider when Talking about the delay. <br> <br>

The Analysis Section which is a very critical section containing Airlines not covered by the top and bottom sections

![analysis](https://user-images.githubusercontent.com/92920156/179708893-79bc8312-5b1f-43a6-b5e7-5ce0471052fe.jpg)

* Airline CO Vs Airline XE <br>
The relationship between Co and XE in terms of delay is very slim in differences though CO has a higher delay which could be related to its slightly longer length travelled than XE. <br> 
The slim differences in their delay could also be related to the huge difference in their flight covered with XE taking the lead. <br>
This is re-establishing the fact that Length is the number determinate of delay of airlines in this datasets. <br>

* Airline FL Vs Airline 9E <br>
The relationship between FL and 9E is another brainstorming scenario. <br>
We are used to a higher delay by an airline whenever the distance/length travelled by that airline is more than that of the other.<br>
But in this case, we would notice that Airline FL travelled the most distance compared to airline 9E yet ended up with a lower delay. <br>
We shouldn't forget their relationship also in terms of flight.<br>
We would notice Airline airline 9E has a higher flight covered compared to airline FL and their difference in distance/length covered is little.<br> <br>

Their fore this accounted for the higher delay in airline Xe with a lesser delay in airline FL. <br>

## Recommendation

With this analytics, I would recommend airline WN the airline with the highest delay to reduce their flight covered which is their main reason for a high delay.<br>
You may be thinking I would have mentioned length but no! <br>

When you compare the analytics of WN and UA you would notice that airline UA has approximately half of the length covered by airline WN with a corresponding approximate 1/12 of her flight..<br>

Leading with a delay difference of over 55,000.<br>

Having seen this you would notice that despite the fact that Length is the number factor when Talking of delay but flight covered is also an important factor that could widen the margin of delay if it's too much… <br>

Though a piece of general advice for all airlines is to copy or imitate the result or methods of which is keeping a balanced ratio between the length and the flight.. <br>
It's advisable that the flight should just be twice the length in order to achieve and beat the result of airline UA and maintain a reasonable delay.<br>

The purpose of an airline is to serve customers and provide utmost satisfaction not dissatisfaction.<br>
Not forgetting that delay is a factor that could lead to dissatisfaction which would result in a reduction in patronage and finally a decline in revenue.<br>






---
# Note
This analytics is based on Length and flight in relationship with the way they affect delay.
Other factors would have been considered but that is beyond the scope of the dataset provided. <br>
Also take note that the 
File uploaded is a power BI template due to large size of the original file
