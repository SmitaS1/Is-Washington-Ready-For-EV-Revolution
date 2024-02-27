# Project_1

# Project Idea

Is Washington Ready for the EV Revolution?

# Data Source

https://rapidapi.com/letscrape-6bRBa3QguO5/api/ev-charge-finder
- Charging Location 

https://fueleconomy.gov/feg/tax2023.shtml
- Tax Incentives 2023

https://catalog.data.gov/dataset/electric-vehicle-population-data
- Washington State Data


# Group Members 
Esha Patel, Ipsita Pattanaik, Jeff Morgan, Neil Lawren, Smita Shah
### PROJECT OUTINE

* Select the real-world data set from API/any other source.
* Download the dataset and convert it into a Pandas DataFrame.
* Perform data cleaning/deal with missing values using Pandas and NumPy.
* Plot interactive graphs to understand the data using visual libraries like matplotlib and hvplot.
* Ask and Answer questions from the dataset.


# Sub-Questions to be answered
1. Which cities in Washington have the most electric and plug-in-hybrid cars registered?
2. What is the ratio of cars to chargers in the selected cities? 
    - What is the availability of fast and slow charging ports per city?
3. What are the most popular car models in the selected cities and do they have federal incentive?

# Analysis
### Sub-QUESTION 1 ANALYSIS: Which cities in Washington have the most electric and hybrid cars registered?
#### Data Overview:
-	Total Rows: 159,106
-	Analysis Focus: Electric and Plug-in Hybrid Vehicles in Washington State, Top 5 Cities 

#### Data Analysis Steps:
-	Grouped data by city and state.
-	Counted VIN (1-10) for each city.
-	Identified top 5 cities with the highest counts.
-	Filtered cities with more than 5000 registered cars.

#### Top 5 Cities with most Electric Vechicles:
-	Bothell, Vancouver, Redmond, Bellevue, and Seattle.

#### Visualizations:
##### Bar Chart 1: Top 5 Cities with Highest EV and Plug-in-hybrid Cars Registered
-	Represents the top 5 cities based on registered electric and plug-in hybrid vehicles.
  
![output](output_data/Top_5_Cities.png) 

##### Bar Chart 2: Total Chargers Available by Cities
-	Represents the total number of chargers available in the top 5 cities. The bar chart helps indicates the charging infrastructure in these cities.

![output](output_data/Total_Chargers_Available_by_Cities.png) 

#### Analysis: 
-	Bothell, Vancouver, Redmond, Bellevue, and Seattle emerge as key cities with significant car registrations.
-	This analysis provides insights into the distribution of electric and plug-in hybrid vehicles and the corresponding charging infrastructure in the specified top 5 cities in Washington State with highest number of registered cars.

### Sub-QUESTION 2 ANALYSIS:  What is the ratio of cars to chargers in the selected cities? What is the availability of fast and slow charging ports per city?
#### Reading Data:
-	The data is read from a CSV file and stored in the chargers_df DataFrame.

#### Filtering Data:
-	We have executed filters on the data for charging stations located in Bellevue, Bothell, Seattle, Vancouver, and Redmond, WA and storeed it in the relevant variables. 

#### Pie Chart:
- A pie chart is created to visualize the distribution of charging speeds for the selected top 5 cities with the greatest population of electric vehicles.

<div id="image-table">
    <table>
	    <tr>
    	    <td style="padding:10px">
        	    <img src="output_data/Bellevue_Charging_Speed_Distribution.png" width="400"/>
      	    </td>
            <td style="padding:10px">
            	<img src="output_data/Bothell_Charging_Speed_Distribution.png" width="400"/>
            </td>
            <td style="padding:10px">
            	<img src="output_data/Redmond_Charging_Speed_Distribution.png" width="400"/>
            </td>
        </tr>
    </table>
</div>

<div id="image-table">
    <table>
	    <tr>
    	    <td style="padding:10px">
        	    <img src="output_data/Seattle_Charging_Speed_Distribution.png" width="400"/>
      	    </td>
            <td style="padding:10px">
            	<img src="output_data/Vancouver_Charging_Speed_Distribution.png" width="400"/>
            </td>
        </tr>
    </table>
</div>

- A pie chart was also created to show charger distribution and car to charger ratio for the selected top 5 cities with the greatest population of electric vehicles. 

<div id="image-table">
    <table>
	    <tr>
    	    <td style="padding:10px">
        	    <img src="output_data/Car_to_Charger_Ratio_per_city.png" width="500"/>
      	    </td>
            <td style="padding:10px">
            	<img src="output_data/Charging_Speed_Distribution.png" width="500"/>
            </td>
        </tr>
    </table>
</div>

#### Map Plot:
- A map plot using hvplot.points is created to display the availability of charging stations near the selected cities on a map.
<div id="image-table">
    <table>
	    <tr>
    	    <td style="padding:10px">
        	    <img src="output_data/Charging_Stations_in_Bellevue.png" width="400"/>
      	    </td>
            <td style="padding:10px">
            	<img src="output_data/Charging_Stations_in_Bothell.png" width="400"/>
            </td>
            <td style="padding:10px">
            	<img src="output_data/Charging_Stations_in_Seattle.png" width="400"/>
            </td>
        </tr>
    </table>
</div>

<div id="image-table">
    <table>
	    <tr>
    	    <td style="padding:10px">
        	    <img src="output_data/Charging_Stations_Vancouver.png" width="400"/>
      	    </td>
            <td style="padding:10px">
            	<img src="output_data/Charging_Stations_Redmond.png" width="400"/>
            </td>
        </tr>
    </table>
</div>

#### Analysis: 
- The analysis shows that overall the top 5 cities have more than 60% of slow chargers. Based on the data, we think that the cities need more fast chargers as it would not be sustainable if there were more electric cars registered per city. 

### Sub-QUESTION 3 ANALYSIS: Question 3: What are the most popular car models in the selected cities and do they have federal incentive?
#### Reading Data:
-	The data is read from a CSV file and stored in the tax_rebate_per_model_compressed_df Dataframe.

#### Merging Data:
-	We have merged the tax rebate data with our top 5 cities dataframe to calculate total for all top car models for selected 5 cities.

#### Bar Chart: Most Popular Car Models in all 5 Cities and WordCloud:
-	Represents the top 6 car models for all selected cities.
  
<div id="image-table">
    <table>
	    <tr>
    	    <td style="padding:10px">
        	    <img src="output_data/Most_popular_car_models.png" width="500"/>
      	    </td>
            <td style="padding:10px">
            	<img src="output_data/WordCloud.png" width="500"/>
            </td>
        </tr>
    </table>
</div>

#### Analysis: 
- Based on our analysis, the most popular car choosen by buyers in selected cities is the TESLA Model Y. It  has a federal incentive of $7,500. We found that not all electric cars are eligible for federal tax incentives. 

### MAIN ANALYSIS: Is Washington Ready for the EV Revolution?
- Based on our research and provided the data, we do not think Washington State is ready for the EV Revolution yet. In our project, we have analyzed the top 5 cities with the most electric vehicles registered and we found that there are not enough charging stations available. High-speed charging can adversely impact the lifespan of a car's battery. Nonetheless, the majority of cars are equipped with an integrated battery management system designed to regulate both the charging speed and the temperature of the battery. Most of the charging stations are slow in charging speed which would not be convenient for everyone specially those who do not have charging stations near their homes and workplaces which will result in issues like cars not having sufficient charge when needed.
- When purchasing an EV vehicle, it is important to know if there are any federal and state incentives provided.

# Limitations 
- Due to the limitation of time and funds, it restricts the depth and thoroughness of the analysis that can be performed. Most of the data available required a lot of funding which we did not have to complete the project.  
- Another challenge was data acquisition. We were unable to find datasets for free. There are chances that our free datasets may be incomplete or outdated, affecting the accuracy of the analysis. 
