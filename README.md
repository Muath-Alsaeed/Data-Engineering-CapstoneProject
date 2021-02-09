 Data Engineering CapstoneProject
 -------------------------------------------
 
 Project Summary:
 -------------------
 This project aims to be able to answers questions on US immigration such as what are the most popular cities for immigration, by builds a data lake using Pyspark that can help to support the analytics by extracting data from all the sources. 
 
 Datasets :
 ------------------------
I94 Immigration Data: This data comes from the US National Tourism and Trade Office , [This](https://travel.trade.gov/research/reports/i94/historical/2016.html)  is where the data comes from.

World Temperature Data: This dataset came from Kaggle. You can read more about it [here](https://www.kaggle.com/berkeleyearth/climate-change-earth-surface-temperature-data).

U.S. City Demographic Data: This data comes from OpenSoft. You can read more about it [here](https://public.opendatasoft.com/explore/dataset/us-cities-demographics/export/).

Airport Code Table: This is a simple table of airport codes and corresponding cities. It comes from [here](https://datahub.io/core/airport-codes#data).

Data Model:
-----------------
use star schema as our data model because Starr schemas are designed to optimize user ease-of-use and minimizing the number of tables join to do the query. 

schema:
----------------------
Dimension Tables :

    city_df
        'City_Name',
         'State_Name',
         'Median_Age',
         'Male_Population',
         'Female Population',
         'Total_Population',
          'State_Code',
           'Race',
         'count_of_Race_in_city'
       
    
    immigrant_df
        
    
    city_temp_df
        'AverageTemperature'
        'City'
    
    ariport_df
        id'
        'type'
        'name'
        'iso_country'
         'local_code'
         'coordinates'
         
        
        
    
Fact Table

    immigration_df:
        id
        state_code
        city_code
        Date
        count



