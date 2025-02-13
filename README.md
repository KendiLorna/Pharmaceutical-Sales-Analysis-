# Pharmaceutical-Sales-Analysis-
A descriptive analysis of sales data from a pharmaceutical company(2017-2020)

### OVERVIEW
The dataset on pharmaceutical sales was obtained from Kaggle.
[Pharmaceutical sale dataset](https://www.kaggle.com/datasets/krishangupta33/pharmaceutical-company-wholesale-retail-data)

The descriptive analysis aimed to uncover trends in sales by time, country, sales representative, channel, product class, etc.

It aimed to show product performance as well as sales reps, and managers' performance.

The insights gained can help in planning for manufacturing/supply chain and allocating marketing resources, training, and incentives for sales teams.

### Data Cleaning and Preparation

I imported the CSV file into Power BI and inspected the dataset in Power Query Editor:
Checking for missing or inconsistent data in key columns using column quality and column distribution features.
Checked for duplicate entries(none were found)
Ensured columns have the correct data types for analysis. 

### Data Modelling

I calculated the following measures:

o	Total Sales

````Total sales = SUM('pharma-data'[Sales])  ````

o	Quantity sold

````Quantity sold = SUM('pharma-data'[Quantity]) ````

o	Customer count

```` Customer Count = DISTINCTCOUNT('pharma-data'[Customer Name]) ````

o	Distributor count

```` Distributor Count = DISTINCTCOUNT('pharma-data'[Distributor]) ````

o	Sales representative count

````Sales rep count = DISTINCTCOUNT('pharma-data'[Name of Sales Rep]) ````

o	Average sales

``` Average sales = AVERAGE('pharma-data'[Sales]) ```

o	Product count

````Product count = DISTINCTCOUNT('pharma-data'[Product Name]) ````

### Visualization Creation
1.	Cards: 
To visualize major metrics such as customers, distributors, total sales, etc.
2.	Map Visualization: 
To visualize sales by country and city bubble size was used to indicate sales volume.
3.	Line Chart: 
To display monthly sales trends.
4.	Bar Chart: 
Compare sales performance by sales rep.
5.	Pie Chart: 
To show the percentage contribution of each product class to total sales.
6.	Table: 
Display aggregated sales data by team and sales manager.
7.	Slicers: 
By country, channel, team, and year to filter the visualizations for a granular view.

### Dashboard

![Pharma sales dashboard](https://github.com/user-attachments/assets/292d6582-0778-4b2f-93fb-b7ccaf8b4ebc)

### General observations

The dataset contains sales data from the year 2017 – 2020 with an average of $46,000 per month in sales

There are four sales teams: Alpha, Bravo, Charlie, and Delta.

There are four managers, one for each team, and 3 sales reps per team except for Delta which has four.

The two sales channels are hospitals and pharmacies.

The hospital channel is further classified into two sub-channels: government and private while pharmacies are classified into retail and institution.

Two countries are responsible for the company sales: Germany and Poland.

There are 240 products divided into 5 classes antibiotics, antipyretics, antimalarials, antiseptics, mood stabilizers, and analgesics.

### Insights and Findings

1. From 2017 to 2020 there is a total sales of $ 12 billion and a total quantity of 29M products sold.
In 2018 the sales peaked at 4 billion dollars while the other years have been at 3 billion dollars.
There is a notable decline in sales from an average of 225 million in 2019 to 205 million in 2020 .

2. The month of August had peak sales overall but this varied per year with June in 2017, March in 2018, August in 2019, and December in 2020.
There seems to be no discernible pattern here.

3. The top-performing product class is analgesics which accounts for 20.19% of sales at a value of $2.3 billion(2017-2020)
while the least-performing products are antimalarials at a value of $1.4 billion for the same period.

4. Antiseptic sales topped in 2020 which could be explained by the Covid-19 pandemic while analgesics peaked overall.

5. Germany is responsible for over 90% of the total sales with products sold in 549 cities and all the sales from Poland are from 2018 only and 200 cities.

6. Hospitals account for 5.5 billion dollars in sales with government hospitals responsible for 45% of sales and private hospitals 55%.
Pharmacies account for 6.2 billion dollars with 55% of the sales coming from retail while the 45% is from institutions.

8. Delta which has four sales reps also has the highest sales record at 3.6 billion dollars.
The manager in charge of the team is Brittany Bold. The bottom team in sales is alpha at 2.5 billion dollars led by James Goodwill.

9. Overall, the top performing sales representative is Jimmy Grey of team Charlie at 986 million dollars, and Allan Ray is at the bottom with 843 million dollars.
Each team has a top-performing sales representative as follows: Alpha - Erica Jones, Bravo - Abigail Thompson, Charlie - Jimmy Gray, and Delta - Sheila Stones.

### Recommendation

Planning marketing activities and budget allocation should be based on region, channel, and products performance.

Measure the impact of marketing campaigns on prescription and sales increases by comparing sales before and after promotional activities (discounts, free samples).

Regulatory and compliance monitoring- sales trends can inform the impact of recalls on sales.

Inventory and supply chain optimization - forecast demand trends to prevent overstocking or stockouts.

Assess how competitor activity affects drug sales.

Further investigation into customer and prescription behavior to identify the most prescribed drugs and trends in physician prescribing habits.

Segment customers (hospitals, pharmacies) based on purchase frequency and volume for focused marketing.

Analyze repeat vs. new customers to determine brand loyalty.

Sales performance analysis to identify top-performing drugs and sales reps based on revenue and sales volume, regions, and seasons.




