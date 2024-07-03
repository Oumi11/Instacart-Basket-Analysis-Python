![instacart_logo](pictures%20and%20visualization/instacart_logo.png)


# Instacart Basket Analysis with Python
### This project was completed as part of the curriculum from the CareerFoundry bootcamp.

## Introduction
### Instacart is an online grocery store, based in the US, that operates through a mobile app. The company makes already good profit and is now focused on analyzing their sales patterns, customer profiles, and purchasing behaviors.

## Business Understanding & Purpose

By analyzing shopping habits and identifying different customer profiles, Instacart can develop targeted marketing strategies. The main goal is to attract more customers, keep them engaged, and boost sales by reaching various customer groups with relevant and effective marketing campaigns.
The aim of this exercise is to utilize Python for cleaning, aggregating, categorizing, and visualizing data, based on [Instacart Online Grocery Shopping Dataset 2017](www.instacart.com/datasets/grocery-shopping-2017) (via Kaggle, on the 03/06/2024).

## Data & Tools
### 1)	Datasets
For the purpose of this exercise multiple datasets have been merged together:
- Customers
- Departments
- Orders
- Products
### 2)	Python libraries
- Pandas
- Numpy
- Seaborn
- Matplotlib
- Spicy

## Key Questions and Findings
### Below are some of the key questions addressed in this project to provide an overview. The Python scripts can be found in the folder 03.Scripts, and the detailed final report is available under the title "Instacart Final Report".

### _1. The sales team needs to know what the busiest days of the week and hours of the day are (i.e., the days and times with the most orders) in order to schedule ads at times when there are fewer orders._

To optimize ad scheduling, it's important to consider the busiest days and times for orders. The graph **shows that Saturdays and Sundays have the highest order volumes**, likely due to users having more free time on weekends. The histogram indicates **a significant peak in orders between 10 AM and 3 PM**, with consistently high orders extending into the evening. Conversely, the **early morning hours between 12 AM and early morning see the fewest orders**. **Therefore, scheduling ads during the early morning hours and on weekdays before the weekend could effectively direct users to make purchases during peak ordering times**.

![num_ords_per_week](pictures%20and%20visualization/num_ords_per_week.png)   ![freq_ords_hour](pictures%20and%20visualization/freq_ords_hour.png) 

### _2.  Are there particular times of the day when people spend the most money? This information might inform the sales team the type of products they advertise at these times._

When looking at the chart of spending per hour, it shows that customers tend to **spend the most money early in the morning and late in the evening**, **with a noticeable dip in spending during the late morning hours around 9-10 AM**. Spending stabilizes in the afternoon and slightly increases again towards the end of the day, **peaking around 8 PM**. With this information in mind, **it is advised to advertise higher-priced products early in the morning and late in the evening when customers are more likely to spend more money.**

<img src="pictures%20and%20visualization/spending_per_hour.png" alt="spending_per_hour" width="400">



### 3. _Instacart has a lot of products with different price tags. Marketing and sales want to use simpler price range groupings to help direct their efforts._

During the analysis, a new column was created by using conditional logic to categorize the products into three different price ranges

![price_range_loc_code](pictures%20and%20visualization/price_range_loc_code.png) 


### _4. Are there certain types of products that are more popular than others? The marketing and sales teams want to know which departments have the highest frequency of product orders._

The graph shows that the departments with the **highest order amounts are produce, dairy and eggs, snacks, and beverages.**
**Directing marketing efforts towards the departments with less than 5% market share** could make a significant difference.

<img src="pictures%20and%20visualization/shares_department.png" alt="shares_department" width="500">

### _5. Is there a connection between age and family status in terms of ordering habits?_

On average, **divorced/widowed middle age users are the ones spending the most**, followed by young adult living with parents and siblings and married adult.

<img src="pictures%20and%20visualization/heat_map_famstat_age.png" alt="heat_map_famstat_age" width="400">

### _6. What differences can you find in ordering habits of different customer profiles?_

When examining the ordering habits of different customer profiles, we find several notable differences. In general, **ordering habits across different departments are quite similar, as they mostly consist of essential grocery products**, which are needed by all customer categories.

However, significant differences emerge when looking at income categories. **High earners, who form a smaller group, tend to spend less overall.** To increase their share, Instacart could **offer a greater variety of high-range products**. This strategy should be balanced by **providing promotions to other income groups when setting up ads**.

For increasing orders in the **bulk product category** for example, **targeting ads at adults or middle-aged adults who are married with dependents could be effective**.

Lastly, **offering incentives** such as loyalty points or bonuses could encourage customers to return more frequently, fostering customer loyalty.

