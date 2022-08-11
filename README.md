# NYC-Citi-Bikesharing
# Purpose 

Purpose: The purpose of the current analysis is to prepare visualizations that give potential investors a look into the highly-successful NYC Citibike bike-sharing program, so that they can see for themselves that a bike-sharing program in Des Moines is a solid business proposal. Among others, we have prepared visualizations that: 
1) Show the length of time that bikes are checked out for all riders and genders 
2) Show the number of bike trips for all riders and genders for each hour of each day of the week, and 
3) Show the number of bike trips for each type of user and gender for each day of the week

# Deliverable 1:  
## Change Trip Duration to a Datetime Format
 
### Results with detail analysis:

1. **The data in the "tripduration" column is converted to a datetime datatype and has the correct time format.**


> Image with `Jupyter Notebook` & `Tableau` Code below.

**Code and Image**


````py
# CHALLENGE 14
### MODULE 14 - Des Moines - Bike Sharing Project
#### By Emmanuel Martinez

import pandas as pd

# 1. Create a DataFrame for the 201908-citibike-tripdata data. 
citibike_df = pd.read_csv(citibike_data)

# 2. Check the datatypes of your columns. 
citibike_df.dtyoes

# 3. Convert the 'tripduration' column to datetime datatype.
citibike_df['tripduration'] = pd.to_datetime(citibike_df['tripduration'], unit='s')

# 4. Check the datatypes of your columns. 
citibike_df.dtypes
````
## Comparison and Analysis of change of datatypes 
(Figure 1) | (Figure 2)
:------------------------------------------:| :-------------------------------------:	
![](img/jupyter_pre.png) | ![](img/jupyter.png)
tripduration presents as an int64 data type.  | tripduration presents as a datetime data type.



2. **The DataFrame is exported as a new file without the index column.**

````py
# 5. Export the Dataframe as a new CSV file without the index.
citibike_df.to_csv("201908-citibike-tripdata_2.csv", index = False)

````
