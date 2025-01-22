# EDA-capstone-project-2
#   Hotel Booking Analysis 
#  **Objective**

The main objective is that to perform EDA on the given dataset and draw useful conclusions about general trends in hotel bookings and how factors governing hotel bookings interact with each other and which is the best time for booking .


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
- country: Country of origin of customers (as mentioned by them)
- market_segment: What segment via booking was made and for what purpose.
- distribution_channel: Via which medium booking was made.
- is_repeated_guest: Whether the customer has made any booking before(0 for No and 1 for Yes)
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

#   Data preparing and cleaning
1.  Check is there any null value or missing values.
   
     a. In this dataset we get 112593 null value in 'company' column so we have replaced the null values with 0.
    
     b. In the 'agent' column we have also get 16340 so we have replaced it with 0.
    
     c. In country we can not set the country values as 0 becuase it contains country codes representing different countries. So instead of replacing it with zero we have     replaced it with the mode value in country column. Mode is nothing but just the most repeating value.
    
     d. Children Column has the count of children then we replaced missing values with mean values.
3. Dropping some coloumn which does not make any sense Several rows in the dataset contains values that does not make any sense like having no adults, children and babies so we directly deleted it by using drop.
4. Change the data type Check the types of datatypes and converting it into int64.

# Exploratory Data Analysis (EDA)
1. Which type og hotel books more (City Hotel or Resort Hotel)?
2. How many booking cancelled ?
3. In which week number of stays is more?
4. In which month has the highest Rooms booked?
5. How many guest are repeated guest?
6. Market segment wise booking?
7. From which country people booked more rooms?


# Conclusion

1- Repeated guest maximum comes from corporate sector.

2- City hotel seems to be more preferred among travellers and it also generates more revenue & profit.

3- Most of the guests stay 3-4 days in the hotel.

4- Most numbers of bookings are made in month of july and august as compared to another month.

5- Room type A is most preferred room as compare to other rooms.

6- Most number of bookings are made fromm Portugal & Great Britain.

7- City hotel guest retains more number of guests.

8- Around one-fourth of the total bookings getting cancelled. More cancellation comes from City hotel.

9- New guest tends to cancel bookings more than repeated customers.

10- Waiting list customers does not affect on their cancel bookings

11- The length of the stay decreases as ADR increses probably to reduce the cost.
