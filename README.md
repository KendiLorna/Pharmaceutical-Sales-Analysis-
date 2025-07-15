# Pharmaceutical-Sales-Analysis-
Detailed analysis of sales data from a pharmaceutical company(2021-2024)

### OVERVIEW
The dataset on pharmaceutical sales was obtained from Kaggle.
[Pharmaceutical sale dataset](https://www.kaggle.com/datasets/krishangupta33/pharmaceutical-company-wholesale-retail-data)

I edited it to include a date column.

The descriptive analysis aimed to uncover trends in sales by time, country, sales representative, channel, product class, etc.

It aimed to show product performance as well as sales reps, and team performance.

The insights gained can help in planning for manufacturing/supply chain and allocating marketing resources, training, and incentives for sales teams.

### Data Cleaning and Preparation

I imported the CSV file into Power BI and inspected the dataset in Power Query Editor:
Checking for missing or inconsistent data in key columns using column quality and column distribution features.
Checked for duplicate entries(none were found)
Ensured columns have the correct data types for analysis.

### Data Modelling

I created a Date table to filter the data dynamically and connected it to the pharma_sales dataset.

I calculated the following measures:

o	Total Sales

````Sales_Total = SUM(pharma_sales[Sales])  ````

o	Quantity sold

````Sales_Quantity = SUM(pharma_sales[Quantity]) ````

o	Customer count

```` Customers_Count = DISTINCTCOUNT(pharma_sales[Customer Name]) ````

o	Distributor count

```` Distributor_Count = DISTINCTCOUNT(pharma_sales[Distributor]) ````

o	Sales representative count

````Rep_Count = DISTINCTCOUNT('pharma_sales'[Name of Sales Rep]) ````

o	Product count

````Product_Count = DISTINCTCOUNT(pharma_sales[Product Name]) ````

o	Preceeding year sales

```Revenue Previous Year = 
CALCULATE(
    [Sales_Total],
    FILTER(
        ALL('Date'),
        'Date'[Year] = MAX('Date'[Year]) - 1
    )
)
 ```
o	Year over Year Percentage Growth

````Latest YoY % Change = 
VAR LatestValue =
    CALCULATE(
        [YoY % Change (Formatted)],
        FILTER(
            ALL('Date'[Year]),
            'Date'[Year] = MAX('Date'[Year])
        )
    )
RETURN
FORMAT(LatestValue, "+0.00%;-0.00%;0.00%")
 ````

### Visualization Creation
1.	Cards: 
To visualize major metrics such as customers, distributors, total sales, etc.
2.	Funnel chart: 
To visualize sales by product class eg antibiotics.
3.	Line Chart: 
To display monthly sales trends.
4.	Bar Chart: 
Compare sales performance by the top five sales representatives.
5.	Pie Chart: 
To show the percentage contribution of each sales team to total sales.
6.	Bar chart with drill down features: 
Display sales by the two channesl-pharmacy and hospital and further by four sub-channels.
7.	Slicers: 
By country, channel,sub_channel, team, and year to filter the visualizations for a granular view.

### Dashboard
Pharma sales dashboard<img width="1402" height="780" alt="Pharma dashboard" src="https://github.com/user-attachments/assets/9ab0dfef-1706-487b-9346-a7ecc7d0e2fa" />



### General observations

The dataset contains sales data from the year 2021 – 2024 with an average of $46,000 per month in sales

There are four sales teams: Alpha, Bravo, Charlie, and Delta.

There are four managers, one for each team, and 3 sales reps per team except for Delta which has four.

The two sales channels are hospitals and pharmacies.

The hospital channel is further classified into two sub-channels: government and private while pharmacies are classified into retail and institution.

Two countries are responsible for the company sales: Germany and Poland.

There are 240 products divided into 5 classes antibiotics, antipyretics, antimalarials, antiseptics, mood stabilizers, and analgesics.

### Insights and Findings

1. From 2021 to 2024 there is a total sales of $11.8 billion and a total quantity of 29M products sold.
There is a 95.48% growth in sales in 2022 from 2021. The increase from 2023 to 2023 is 3.24% and 2.84% the following year.

2. The month of December had peak sales overall with peak sales in November 2021 and December in 2022,2023, and 2024.
There i'snt a huge variance in monthly sales but the last quarter is the best performer saleswise.

3. The top-performing product class is analgesics which accounts for 20.19% of sales at a value of $2.4 billion(2021-2024)
while the least-performing products are antimalarials at a value of $1.5 billion(12.5%) for the same period.

4. Product performance is fairly stable with antimalarials remaining the least selling, Analgesics peak in 2022 and 2023 while antiseptics peak in 2021 and 2024.

5. Germany is responsible for over 90% of the total sales with products sold in 549 cities and all the sales from Poland are from 2021 only and 200 cities.
The company might have pulled out of that market.

6. Hospitals account for $5.6 billion(52.5%) in sales with government hospitals responsible for 45% of sales and private hospitals 55%.
Pharmacies account for $6.2 billion(47.5%) with 55% of the sales coming from retail and 45% from institutions.

7. Delta which has the highest number of sales reps also has the highest sales record at $3.6 billion.
The manager in charge of the team is Brittany Bold. The bottom team in sales is alpha at $2.6 billion led by James Goodwill.

8. Overall, the top-performing sales representative is Jimmy Grey of team Charlie at $986 million, and Allan Ray is at the bottom with $843 million.
Each team has a top-performing sales representative as follows: Alpha - Erica Jones, Bravo - Abigail Thompson, Charlie - Jimmy Gray, and Delta - Sheila Stones.

### Recommendation

1. Capitalize on Year-Over-Year Growth Momentum
Sales grew by 95.48% in 2022, followed by a more modest increase in subsequent years.
Investigate what drove the 2022 surge-new products, market entry, or distributor expansion, and replicate what is possible.

2. Strategically align sales promotions with seasonality
December consistently peaks in sales.
Position Q4 as a high-investment period for product launches, discount programs, and awareness campaigns. Develop a monthly baseline to spot underperformance.

3. Product class action.
Analgesics dominate with $2.4B, while Antimalarials lag at $1.5B.
Maintain analgesics’ dominance through brand reinforcements. For antimalarials, explore market education, pricing review, or product reformulation to tap into demand.

4. Geographical presence
Germany accounts for 90%+ of sales; Poland’s activity was limited to 2021.
Assess Poland’s withdrawal and its implications. Look into Germany’s top-performing cities to drive regional replication. Explore other European markets if capacity allows.

5. Customer Segment
Pharmacies (47.5%) and Hospitals (52.5%) split revenue closely.
Enhance engagement with government vs. private hospitals and retail vs. institutional pharmacies. Curate offerings based on purchasing behavior and procurement cycles.

6. Team performance
Team Delta leads at $3.6B, possibly due to size and strategy.
Document best practices under Brittany Bold’s leadership. Apply targeted training to Team Alpha to close gaps, particularly under James Goodwill.

7. Recognition and incentivize the top Sales Representatives
Every team has standout performers.
Encourage top sales reps and managers through incentives and initiate peer-learning initiatives featuring each team’s top rep. This is to cultivate motivation and share winning tactics across teams.

8. Strengthen distribution networks
Only 29 distributors support 751 customers across 240 products, which could lead to a potential bottleneck.
Evaluate distributor capacity and explore onboarding additional partners, especially in underserved regions.
