# Hotel-booking-analysis
## Objective
Our primary goal is to conduct EDA on the provided dataset and derive valuable conclusions about broad hotel booking trends and how various factors interact to affect hotel bookings.
## Dataset
 We get a dataset of hotel reservations. A city hotel and a resort hotel's reservations are included in this dataset. It has the following features:
 - hotel: Name of hotel ( City or Resort)
 - is_canceled: Whether the booking is canceled or not (0 for no canceled and 1 for canceled)
 - lead_time: time (in days) between booking transaction and actual arrival.
 - arrival_date_year: Year of arrival
 - arrival_date_month: month of arrival
 - arrival_date_week_number: week number of arrival date.
 - arrival_date_day_of_month: Day of month of arrival date
 - stays_in_weekend_nights: No. of weekend nights spent in a hotel
 - stays_in_week_nights: No. of weeknights spent in a hotel
 - adults: No. of adults in single booking record.
 - children: No. of children in single booking record.
 - babies: No. of babies in single booking record. 
 - meal: Type of meal chosen 
 - country: Country of origin of customers
 - market_segment: What segment via booking was made and for what purpose.
 - distribution_channel: Via which medium booking was made.
 - is_repeated_guest: Whether the customer has made any booking before(0 for No and 1 for 
                 Yes)
 - previous_cancellations: No. of previous canceled bookings.
 - previous_bookings_not_canceled: No. of previous non-canceled bookings.
 - reserved_room_type: Room type reserved by a customer.
 - assigned_room_type: Room type assigned to the customer.
 - booking_changes: No. of booking changes done by customers
 - deposit_type: Type of deposit at the time of making a booking (No deposit/ Refundable/ No refund)
 - agent: Id of agent for booking
 - company: Id of the company making a booking
 - days_in_waiting_list: No. of days on waiting list.
 - customer_type: Type of customer(Transient, Group, etc.)
 - adr: Average Daily rate.
 - required_car_parking_spaces: No. of car parking asked in booking
 - total_of_special_requests: total no. of special request.
 - reservation_status: Whether a customer has checked out or canceled,or not showed 
 - reservation_status_date: Date of making reservation status.

Total 119390 rows and 32 columns in dataset

## Library used
We have used Python 3 to its following packages:

Pandas
Matplotlib
Seaborn
Sklearn

## Data Cleaning and Feature Engineering:
 [1] Removing Duplicate Values
 - Rows that were duplicates were removed.
 [2] Handling Null / Missing Values
 - Children, country, and agent are discrete numerical variables, so replaced null values with mode of it.
 - Variable company had null values greater than 50%, so removed it.
 [3] Removing Outliers
 - Interquartile Range in the skew symmetric curve used to remove outliers found in the lead_time and adr variables.
 [4] Converting Columns to Appropriate Data Types
 - Datatypes of variables "children," "agent," "reservation_status_date," "total_people," and "total_children" were transformed from float64 datatypes to int64.
 - Datatype of the variable "reservation_status_date" was transformed from object datatype to datetime64.
 [5] Created New Columns
 - The variable "stay_length" is created by adding the variables "stays_in_weekend_nights" and "stays_in_weeknights."
 - The variable "total_person" is created by adding the variables "adults," "children," and "babies."
 - From variables "children" and "babies," a new "kids" variable is created by adding both of them.
 - The variable "total_person" used to create "guest_type."
 ## Exploratory Data Analysis:
 Performed EDA and tried answering the following questions:
 
 Q1) Which hotel is most preferred?
 Q2) Hotel Wise Bookings based on Date and Month also What is the trend of bookings within a month ?
 Q3) Country Wise - Number of Bookings ?
 Q4) Which agent is making maximum Bookings ?
 Q5) Which room type is in most demand and which room type generates the  highest average daily rate?
 Q6) How long do people stay at the hotels?
 Q7) What is preferred stay length in each hotel based on weekday nights and weekend nights ?
 Q8) Cancellation rates in both the hotels?
 Q9) Which room generates highest Average daily rate?
 Q10)Which hotel has longest waiting list?
 Q11) Is thier any Special request given by the customer to hotels?
 Q12) Which channel is mostly used for the booking of hotels? 
 Q13) Which types of customers mostly make bookings?
 Q14) How many customers are most likely to require a parking space?
 Q15)Which customer type generates more revenue in terms of hotel types and customer types?

 Mainly performed using Matplotlib and Seaborn library and the following graph and plots had been used:

 -Bar Plot.
 -Scatter Plot.
 -Pie Chart.
 -Line Plot.
 -Heatmap.
 -Box Plot
 
 ## Conclusion:
  - The top country with the most number of bookings is PRT, and the number one agent with the most number of bookings is 9. 
 - Customers favored city hotels more than resort hotels.
 - One of the four reservations is canceled.
 - The Online (internet) platform is used to make the majority of bookings.
 - The majority of the bookings are made using TA/TO, the leading distribution channel.
 - The customer wants Room A to be reserved the most.
 - Customers favored making a hotel reservation for a short visit.
 - Only of people require space to park their cars.
 - Most visitors are couples.
 - Booking cancellations are not caused by a longer Lead time.
 - A city hotel is busier than a resort.
 - The busiest months for hotels are October and September. There isn't a lengthy wait for reservations in July.
 - Not assigning a reserved room does not affect ADR.

   ## Challenges:
   (1) Lot of null values were present in the dataset.
   (2) It was challenging to select the best visualization techniques.
   (3) Lot of duplicate data.
   (4)The improper data type format was used for the data.
