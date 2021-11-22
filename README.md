
# Hotel Revenue Analysis



## Project Description:
The purpose of this project is to analyse the data of two types of Hotels (specially from the year 2018 to 2021) to answer some business questions mentioned in the requirements given by our stakeholders.
We have been provided with 5 csv files which contain different records about the concerned hotels and using these we need to develop the entire project.



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

![Capture3](https://user-images.githubusercontent.com/80168511/142902129-25c76f10-e78b-4232-a64d-909af86010b4.PNG)

After importing the table looks like--

![Capture2](https://user-images.githubusercontent.com/80168511/142902269-cc4a2b9b-f231-4a64-960e-d05217889374.PNG)

Now we have created another 2 blank tables named-market_segment and meal_cost and to them we have imported data from the respective csv files .These two tables contain the information about the discount provided to the customer of different market segment and cost of meal according to their meal code.The screenshots of the SQL Query and the imported tables are given below:

![Capture4](https://user-images.githubusercontent.com/80168511/142902419-af1abf2d-a4b2-4e3b-ab2a-1785c0f51aaa.PNG)

![Capture5](https://user-images.githubusercontent.com/80168511/142902441-4415e68a-e6f6-4549-9896-5b6472add7fe.PNG)

![Capture6](https://user-images.githubusercontent.com/80168511/142902449-bd368f6e-8e21-4371-8d72-e07120609977.PNG)

Now using SQL Query we can check that in each year which hotel has earned how much total revenue.

![Capture8](https://user-images.githubusercontent.com/80168511/142902775-e0e4f929-52ed-4973-a064-13afaabcc165.PNG)

Now we have created a master table combining every table using union all and left join, which contains data of every year in a single table and also there are columns containing information about meal cost and discount.Then this master table has been connected to the PowerBI for further manipulation and Dashboard building.All the related screenshots are given below:

This master table has also been exported from SQL as a csv file on a name hotel_revenue_mastertable_sql. It is present in my github project file repository.

![Capture9](https://user-images.githubusercontent.com/80168511/142902873-82c3266b-2699-4a09-b841-362af3407ca3.PNG)

This way we will connect to PowerBI

![Capture12](https://user-images.githubusercontent.com/80168511/142903048-c7b1db09-0766-4b4e-8c24-841368c2954c.PNG)

Now in Power Query we have made all the necessery changes like datatype of columns, sorted the country code column(excluded the null rows) ,etc.Then we have added a new column "revenue" to our datatable using custom column and the formula as shown below:

![Capture11](https://user-images.githubusercontent.com/80168511/142903206-954efe09-cd97-47d1-b543-3bf34bfdc864.PNG)

We have also created measures like "Total Nights" and "Parking Percentage"--

![Capture13](https://user-images.githubusercontent.com/80168511/142903414-871c64d3-538a-448e-86c0-e021b024c28b.PNG)

![Capture14](https://user-images.githubusercontent.com/80168511/142903429-abf612b9-f458-444d-bf24-5f6752b3cd6d.PNG)

And finally our final Dashboard contains 2 pages , first page is visualizing the revenue analysis and the 2nd page visualizes the parking space analysis of the hotels for the year 2018 to 2020. In the first page we can check the trend of revenue ,average night or customer are staying ,average discount offered ,average daily rate also we can check the revenue by hotels. From the matrix shown in the 2nd page we can conclude that there is no such evedence that parking space demand is growing by year, it is more or less stagnant , so we don't need to increase our parking lot space.

The final Dashboard looks like--

![1](https://user-images.githubusercontent.com/80168511/142903584-057b9b3c-8958-4f38-98c3-a934a04bde30.PNG)

![2](https://user-images.githubusercontent.com/80168511/142903607-66c03fb5-0133-490b-b1f4-bf5e84b4e4b2.PNG)

