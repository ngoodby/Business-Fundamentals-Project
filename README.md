# Metis Business Fundamentals Project
## City of Boulder EV Charging Station Health Assessment

**Visualizations:**
- The associated Tableau dashboard for this project can be found [here](https://public.tableau.com/views/BoulderEVChargingStations/Dashboard?:language=en-US&:display_count=n&:origin=viz_share_link)
- A tornado chart of failure rates and transactions can be found [here](https://public.tableau.com/views/EVStationTornadoChart/Tornado?:language=en-US&:display_count=n&:origin=viz_share_link)
- A simple chart of station transaction counts can be found [here](https://public.tableau.com/views/BoulderEVTransactionCount2021/NumberofTransactions?:language=en-US&:display_count=n&:origin=viz_share_link)

*Abstract:* This project serves as a preliminary analysis of data from the City of Boulder, Colorado on transactions at City operated electric vehicle charging stations. Charging stations were evaluated based on their use rate as well as the failure rate of their plugs. This analysis motivates potential future work to establish a real-time system of anomaly detection to identify malfunctioning chargers, as well as stations whose data reporting systems may be failing. The impact hypothesis of proposed future work is that the automated detection of plug failures and reporting malfunctions would improve maintenance response time, thereby shortening outages and increasing public use and satisfaction. 

*Design:* The City of Boulder operates 25 electric vehicle charging stations and they are wondering how the stations are performing and how to prioritize the maintenance of the various stations. I built a Tableau dashboard that highlights key insights from existing data on the use and functionality of these stations. My analysis revealed the need to better track, understand, and address data reporting issues and plug performance issues occurring at the City’s charging stations.

*Data:* The [City of Boulder’s data](https://open-data.bouldercolorado.gov/datasets/183adc24880b41c4be9fd6a14eb6165f_0/explore) on electric vehicle charging station energy consumption contains information on 32,635 reported transactions across the City’s 25 charging stations. This data set was combined with [additional information](https://bouldercolorado.gov/services/electric-vehicle-charging-stations#section-8319) on whether the stations cost money to use and how many plugs are available at each station. Plug and rate info could not be found for three stations (1275 Alpine Ave, 5050 Pearl St, & 900 Baseline Rd). As such, those stations were excluded from this analysis, leaving 26,696 relevant transactions. My analysis primarily focused on 2021 data, which included 8,852 relevant transactions.

*Algorithms:* The combined data were used to derive information about failure rates per charging event at each station, which was used to better understand which stations are most in need of maintenance. The data were also used to derive the percent of a given month that a plug at a given station was in use to understand station traffic and plug demand.

*Tools*
•	Python (Pandas, Requests, and Beautiful Soup) to scrape info on number of plugs and fee for each station
•	Geopandas to geolocate lat/long coordinates from addresses
•	Excel to join info on number of plugs and presence of a fee to the main dataset, manipulate data, and generate variables of interest
•	Tableau to create an interactive dashboard of results
