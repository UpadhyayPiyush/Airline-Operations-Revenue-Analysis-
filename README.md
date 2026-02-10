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










