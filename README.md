
# Hotel Revenue Analysis



## Project Description:
The purpose of this project is to analyse the data of two types of Hotels (specially from the year 2018 to 2021) to answer some business questions mentioned in the requirements given by our stakeholders.
We have been provided with 5 csv files which contains different records about the concerned hotels and using these we need to develop the entire project.



## Project Requirements:
We have to create a SQL Database where all the data files of our hotels will be imported. Now we need to manipulate the tables using SQL query to make some analysis about the data.Then this database needs to be connected with the PowerBI,where we have to build a visual data story or dashboard, which we will present to our satakeholder to answer some business questions like--
  1. Is our Hotel revenue growing by year? 
  2. Parking lot size should be increased or not?
  3. What trend we can see in the data (especially the average daily rate,guests to explore seasonality)?


 
## Project Pipeline:

![Slide1](https://user-images.githubusercontent.com/80168511/142891804-2bb51122-8e59-495c-864a-3124b287c4df.JPG)


## Project Walkthrough:
At first we have created a database named-"power_bi_project" and inside it we have created 3 blank tables (hotel_records,hotel_records_2019 and hotel_records_2020).Now we have imported data from the 3 csv files i.e. hotel_revenue_2018,hotel_revenue_2019 and hotel_revenue_2020 to our newly created blank tables- hotel_records,hotel_records_2019 and hotel_records_2020 respectively.The screenshots of the SQL Query is provided below:

![Capture](https://user-images.githubusercontent.com/80168511/142901644-b01c394a-9c22-4562-ba6f-ff8e2d71eb07.PNG)

![App Screenshot](https://snipboard.io/UWyAgK.jpg)

After importing the table looks like--

![App Screenshot](https://snipboard.io/gXpc8m.jpg)

Now we have created another 2 blank tables named-market_segment and meal_cost and to them we have imported data from the respective csv files .These two tables contain the information about the discount provided to the customer of different market segment and cost of meal according to their meal code.The screenshots of the SQL Query and the imported tables are given below:

![App Screenshot](https://snipboard.io/XQWJab.jpg)

![App Screenshot](https://snipboard.io/ISgimY.jpg)

![App Screenshot](https://snipboard.io/XAsVZi.jpg)

Now using SQL Query we can check that in each year which hotel has earned how much total revenue

![App Screenshot](https://snipboard.io/zYn24o.jpg)

Now we have created a master table combining every table using union all and left join, which contains data of every year in a single table and also there are columns containing information about meal cost and discount.Then this master table has been connected to the PowerBI for further manipulation and Dashboard building.All the related screenshots are given below:

This master table has also been exported from SQL as a csv file on a name hotel_revenue_mastertable_sql. It is present in my github project file repository.

![App Screenshot](https://snipboard.io/GYgAtl.jpg)

This way we will connect to PowerBI

![App Screenshot](https://snipboard.io/NhSHU0.jpg)

Now in Power Query we have made all the necessery changes like datatype of columns, sorted the countyr code column(excluded the null rows) ,etc.Then we have added a new column "revenue" to our datatable using custom column and the formula as shown below:

![App Screenshot](https://snipboard.io/k6tvO0.jpg)

We have also created measures like "Total Nights" and "Parking Percentage"--

![App Screenshot](https://snipboard.io/FC0mol.jpg)

![App Screenshot](https://snipboard.io/K53bXx.jpg)

And finally our final Dashboard contains 2 pages , first page is visualizing the revenue analysis and the 2nd page visualizes the parking space analysis of the hotels for the year 2018 to 2020. In the first page we can check the trend of revenue ,average night or customer are staying ,average discount offered ,average daily rate also we can check the revenue by hotels. From the matrix shown in the 2nd page we can conclude that there is no such evedence that parking space demand is growing by year, it is more or less stagnant , so we don't need to increase our parking lot space.

The final Dashboard looks like--

![App Screenshot](https://snipboard.io/19HIMu.jpg)

![App Screenshot](https://snipboard.io/Yq3lxH.jpg)

