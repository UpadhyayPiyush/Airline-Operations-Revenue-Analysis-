# Airline-Operations-Revenue-Analysis

## Project Overview
- Airline Operations & Revenue Analytics
- This project analyzes an airline operational database to evaluate flight performance, passenger behavior, aircraft utilization, and revenue generation.
- The dataset contains 1.04M+ ticket-flight records, 366K+ passengers, 579K+ boarding events, and 33K+ flights across multiple airports and aircraft types.
- The goal is to transform raw operational data into actionable business intelligence by identifying inefficiencies such as low seat utilization, passenger no-shows, and uneven route demand.
- The analysis simulates a real-world airline scenario where a data analyst investigates declining profitability despite high booking activity.

## Business Problem / Challenges
- Operational inefficiency affecting profitability
- Airline revenue appeared inconsistent even though booking activity remained high.
- Nearly half of reserved seats were not utilized due to passenger no-show behavior.
- Several flights operated with very low seat occupancy, increasing operational cost per passenger.
- Aircraft were not always assigned according to passenger demand, leading to capacity mismatch.
- Some routes carried heavy passenger traffic while others operated underutilized.
- Flight scheduling decisions were being made based on bookings instead of actual passenger turnout.

## Objective
- Use operational data to improve airline decision-making
- Measure actual passenger turnout vs booked passengers
- Calculate flight load factor and aircraft utilization
- Analyze delay patterns and route demand
- Identify revenue contribution by fare class and aircraft type
- Detect revenue leakage caused by passenger no-shows
- Provide data-driven recommendations for route planning and capacity optimization

## Database Overview 
**SQLite Airline Operational Database**  
**8 relational tables representing the airline lifecycle:**
- flights → flight schedules and aircraft assignments (33K+ flights)
- ticket_flights → ticket pricing and flight allocation (1.04M+ records)
- tickets → passenger bookings (366K+ passengers)
- boarding_passes → actual boarded passengers (579K+ boardings)
- seats → aircraft seat configuration
- aircrafts_data → aircraft models
- airports_data → departure and arrival airports
- bookings → booking transactions  
**The database models the real passenger journey:**  
**Booking → Ticket → Flight → Boarding → Aircraft → Airport**

## Tools & Technologies 
- Data Analysis Stack
- SQL (SQLite) — querying relational database
- Python
  - pandas → data processing
  - numpy → numerical operations
  - matplotlib → visualizations
  - seaborn → statistical plots
- Jupyter Notebook — analysis workflow
- Data Visualization — business insights reporting

## Findings  

![Visual 1](https://github.com/UpadhyayPiyush/Airline-Operations-Revenue-Analysis-/blob/main/Graphs/Visual%201.png)  
**Passenger Show vs No-Show Distribution**  
The chart indicates that only 55.43% of booked passengers actually boarded, while 44.57% did not travel despite having reservations. This reveals a very high passenger no-show behavior, meaning nearly half of the reserved seats flew empty. The insight suggests inaccurate demand prediction and highlights the need for strategies such as reminder notifications or controlled overbooking to improve seat utilization.  

![Visual 2](https://github.com/UpadhyayPiyush/Airline-Operations-Revenue-Analysis-/blob/main/Graphs/Visual%202.png)  
**Revenue Impact of Passenger No-Shows**  
The airline realized only 55.55% of its expected operational revenue, while approximately 44.45% of potential revenue was operationally lost due to passenger no-shows. Even though tickets were sold, empty seats reduced effective revenue generation and distorted capacity planning. This finding strongly supports implementing predictive overbooking and better passenger confirmation systems to minimize revenue leakage and improve profitability.  

![Visual 3](https://github.com/UpadhyayPiyush/Airline-Operations-Revenue-Analysis-/blob/main/Graphs/Visual%203.png)  
**✈️ Load Factor Distribution Across Flights**  
This histogram shows how full the airline’s flights are in terms of seat occupancy. A large concentration of flights appears at the lower load factor range, meaning many flights are operating with a small percentage of seats filled, while comparatively fewer flights reach high occupancy levels near 70–100%. Overall, the graph indicates that most flights are not fully utilized and a significant portion of seat capacity remains empty across the network.  













