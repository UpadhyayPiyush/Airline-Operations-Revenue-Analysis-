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

![Visual 4](https://github.com/UpadhyayPiyush/Airline-Operations-Revenue-Analysis-/blob/main/Graphs/Visual%204.png)  
**✈️ Average Load Factor by Aircraft Type**  

This bar chart compares the average seat occupancy across different aircraft types. The CN1 aircraft shows the lowest utilization with an average load factor of around 15%, while larger aircraft such as the 733 and 773 achieve higher occupancy levels, reaching approximately 56% and 66% respectively. Overall, the chart indicates that passenger demand varies significantly by aircraft type, with some aircraft consistently operating far less full than others.  

![Visual 10] (https://github.com/UpadhyayPiyush/Airline-Operations-Revenue-Analysis-/blob/main/Graphs/Visual%2010.png)  
**🛫 Top 10 High Demand Routes**  

This bar chart displays the routes with the highest number of passengers across the airline network. The SVO–LED and DME–OVB routes carry the largest passenger volumes, each serving around 9,500+ travelers, while other listed routes still maintain consistently high traffic above roughly 7,500 passengers. The graph shows that passenger demand is concentrated on a limited set of routes, indicating these routes experience significantly heavier travel activity compared to others.  

![Visual 6] (https://github.com/UpadhyayPiyush/Airline-Operations-Revenue-Analysis-/blob/main/Graphs/Visual%206.png)  
**💰 Revenue vs Load Factor Relationship**  

This scatter plot illustrates the relationship between flight seat occupancy (load factor) and the revenue generated per flight. As the load factor increases toward 80–100%, the flight revenue also rises significantly, with the highest revenues observed on flights that are nearly full. The graph clearly shows a positive relationship, indicating that flights with more occupied seats generate substantially higher revenue compared to low-occupancy flights.  

![Visual 7](https://github.com/UpadhyayPiyush/Airline-Operations-Revenue-Analysis-/blob/main/Graphs/Visual%207.png)  
**💺 Revenue Contribution by Fare Class**  

This bar chart shows the total revenue generated from each ticket class. The Economy class contributes the largest share of revenue (around 14+ billion), significantly higher than Business class (about 5+ billion), while the Comfort class contributes only a very small portion. The graph indicates that the airline’s overall revenue is primarily driven by high passenger volume in Economy class rather than premium seating categories.  

![Visual 8] (https://github.com/UpadhyayPiyush/Airline-Operations-Revenue-Analysis-/blob/main/Graphs/Visual%208%20.png)  
**💰 Top 10 Revenue Generating Routes**  

This bar chart presents the routes that generate the highest total revenue for the airline. The DME → KHV and KHV → DME routes produce the maximum earnings, each generating roughly 700+ million in revenue, while the remaining routes also contribute substantial amounts above approximately 400 million. The graph shows that a small group of routes accounts for a significant share of the airline’s total revenue.  

![Visual 9] (https://github.com/UpadhyayPiyush/Airline-Operations-Revenue-Analysis-/blob/main/Graphs/Visual%209.png)  
**✈️ Revenue by Aircraft Type**  

This bar chart shows the total revenue generated by each aircraft model. The SU9 aircraft produces the highest revenue at approximately 5+ billion, followed by the 763 and 773 aircraft, while the CN1 aircraft generates very minimal revenue compared to others. The graph indicates that revenue generation is uneven across the fleet, with certain aircraft types contributing significantly more to overall airline earnings than others.


## Recommendations 

- Data-Driven Operational Improvements
- Implement controlled overbooking using historical no-show patterns
- Use boarding data instead of booking counts for demand forecasting
- Assign smaller aircraft to low-demand routes
- Increase frequency on high-traffic routes
- Review flights operating below 60% load factor
- Prioritize high-volume economy seat occupancy
- Optimize route planning based on actual passenger turnout

## Conclusion

The analysis demonstrates that the airline’s problem is not lack of passengers but inefficient operational planning. A 44% passenger no-show rate, low load factors, and uneven aircraft utilization significantly reduce effective revenue generation.
By aligning aircraft capacity with real passenger turnout and making scheduling decisions based on boarding behavior rather than booking counts, the airline can improve profitability without increasing fleet size or ticket prices.
This project highlights how data analytics can transform operational data into strategic business decisions and improve real-world airline performance.














