# Bikes-and-its-Accessories-Sale-in-Europe
Power BI Dashboard use to Analyse the KPI Requirement, finding and recommendation 

Executive Summary
The present study uses a large dataset that was carefully selected to contain only relevant European countries from Kaggle to give a thorough examination of the European bike sales market over a six-year period, from 2011 to 2016. Precision was prioritized, and the dataset underwent extensive validation to guarantee 100% accuracy and the absence of any missing or unknown data points, providing a strong basis for the study.
Starting with a fact table, the analytical process led to the development of five powerful Power BI dashboards: Sales Performance, Product Performance, Geographic Analysis, Customer Demography, and Operational Insights. These dashboards act as a broad lens, offering a multifaceted perspective on the dynamics of the industry. Three crucial conclusions may be drawn from the dashboards: the prominence of "Bikes" in product sales, the regional differences in sales performance, and the impact of customer demographics on buyer behavior. These observations foretell future trends in addition to reflecting the situation of the industry now. The research suggests concentrating on high-performing areas and goods, creating marketing plans that take client demographics into account, and streamlining operational procedures to increase profit margins in order to make use of these findings. These suggestions are meant to maintain and strengthen market supremacy; they are not just reactive. Rather, they are strategic. This research is proof of the ability of business intelligence solutions like Power BI to turn unstructured data into valuable strategic assets, in addition to synthesizing massive amounts of data into actionable knowledge.
2
Introduction
Maintaining a competitive edge in an increasingly data-driven corporate world requires the ability to effectively evaluate and analyze sales data. This research is the result of a comprehensive analysis of bike sales throughout Europe, which was carried out with the objective of reducing complex datasets into insightful analysis that can guide strategic decision-making. This analysis, which makes use of the most recent business intelligence techniques, aims to provide a comprehensive narrative of the market dynamics at work by addressing important concerns like product performance, consumer preferences, and operational efficiency. This report is based on a dataset that was carefully collected from Kaggle, a website that is well-known for having enormous collections of high-quality, real-world data. The dataset was selected due to its extensive coverage of bike sales data, encompassing a variety of indicators from total revenue to unit sales, in France, Germany, and the UK. The dataset was subjected to stringent validation procedures before analysis to guarantee total integrity, with an emphasis on the European market by eliminating data from irrelevant locations like the USA. This degree of accuracy in data processing highlights the report's dedication to relevance and dependability. This report is presented through five dashboards that were made with Microsoft's interactive data visualization tool, Power BI. The report's main pillars are these dashboards: Sales Performance, Product Performance, Geographic Analysis, Customer Demography, and Operational Insight. They offer a methodical and perceptive analysis of the sales data. They become a story that speaks volumes about customer behavior, industry trends, and business potential, rather than merely being reflections of numerical data.
While the Product Performance dashboard focuses on the specifics of individual product categories and their relative contributions to overall sales, the Sales Performance dashboard analyzes trends and health of sales overall. The sales distribution across different regions is depicted in the Geographic Analysis dashboard, providing an indication of future market expansions or contractions. To enable more focused marketing tactics, Customer Demography further segments the sales data based on several demographic parameters. Finally, a critical assessment of the sales operations is given by the Operational Insight dashboard, which pinpoints areas where efficiency can be increased.
Readers will obtain a thorough grasp of the European bike sales scene from 2011 to 2016 by working through this research. Businesses trying to enhance profitability, improve customer understanding, and optimize sales methods can find great guidance from the insights offered. This research, which carefully combines business intelligence with data analytics, is proof of the transformational power of data when used wisely.
3
Data Pre-Processing and Data Cleansing
This business intelligence project began with a thorough pre-processing and cleaning of the data, which was essential to guaranteeing the dataset's correctness and suitability for thorough analysis. This dataset, which came from Kaggle, needed to be carefully prepared for the in-depth analysis that was about to take place.
Removing NAs: To begin with, the dataset was thoroughly scanned in order to find and eliminate any "Not Available" (NA) entries. Inaccurate results and unbalanced analysis can arise from the presence of NAs. Nonetheless, the validation of the dataset verified a 100% data integrity score, signifying the absence of any null or missing values in the dataset. The uniqueness and completeness of the dataset were maintained because this uncommon example of a clean dataset eliminated the requirement for imputation or the removal of missing data.
Renaming Columns: Column names were standardized in order to simplify the data and provide a more intuitive analysis. This step was essential to preventing misunderstandings and guaranteeing that the content of each column was immediately apparent. Clarity and consistency were prioritized during the renaming process in order to conform to Power BI's naming guidelines and improve the dataset's usability for users with varying degrees of
4
data literacy.
Changing Data Types: Another important step that was made was to correct the data types. This process included precisely categorizing categories data, making sure dates were formatted correctly, and translating texts to numeric values where necessary. Data type alignment is critical because it impacts the dataset's interoperability with Power BI's analytical features, which are capable of identifying and processing multiple data types.
5
Removing Errors: Possible mistakes in the dataset were found and fixed. This includes data input errors, such as misspellings of product names or incorrect categorization. To maintain a homogeneous dataset—which is essential for any kind of comparison analysis—such differences were addressed.
6
Removing Columns: Since the investigation focused on bike sales in Europe, the dataset was culled of unnecessary columns, especially those that mentioned non-European countries like the USA. This improved the dataset's relevance and streamlined it, making it easier to handle and speeding up Power BI's processing speeds.
7
Merging Tables: Initially, the sales data was dispersed over several tables, requiring a combining procedure. A vital stage in this procedure was the production of an extensive fact table. In order to provide a more in-depth study, the fact table was created to incorporate multiple data dimensions, including time, product, and location. A relational
8
model, which is essential for carrying out multidimensional analysis in Power BI, was developed by combining tables and establishing suitable linkages between them.
These painstaking phases of data pre-processing and purification turned the dataset into a superior building block for the BI project stages that followed. By following these procedures, it was guaranteed that the data was ready to be transformed into perceptive visualizations and that the conclusions drawn from them were grounded in the most precise and pertinent data.
9
Data Modeling – Facts and Dimensions
Data modeling is an essential phase in the Business Intelligence (BI) process that converts unprocessed data into insights that can be put to use. Because of its ease of use and efficiency in managing intricate queries, the Star Schema is a model that is frequently used in data warehousing systems. It has a primary fact table (European Bicycle Sales) that links to other dimension tables, including those for product, location, details about the customer, and sales date. This design makes it possible to query big datasets for analytical purposes in an efficient and organized manner.
Creating and Modifying Relationships: 'BIKE SALES IN EUROPE' was the major fact table created as part of the data modeling process for the European bike sales data. Important performance indicators like cost, order quantity, profit, and sales efficiency are listed in this table. The foundation of the Star Schema is the fact table, which has connections to many dimension tables and contains quantitative data that may be studied in different slices.
Dimension tables with the titles "PRODUCT," "CUSTOMER LOCATION," "SALES DATE," and "CUSTOMER DETAILS" surround this fact table. These tables include attributes, like product categories, consumer demographics, and sales date information, that are exclusive to their individual entities. Using main and foreign keys, new associations were created between each dimension table and the fact table. An analysis of sales data by
10
various product categories was made possible, for example, by linking 'PRODUCT_ID' from the PRODUCT table to the equivalent 'PRODUCT_ID' in the fact table.
To maintain data integrity and maximize query efficiency, it was also essential to modify current associations. For accurate analysis, it is essential that there exist matching values in both tables of a connection, which was accomplished by enforcing referential integrity and specifying the proper cardinality.
Normalizing Data: Large tables were standardized into smaller, more focused tables in order to reduce data redundancy and improve data integrity and streamline the data model. To separate demographic information from geographic information, a monolithic table with customer information might be split into two sections: "CUSTOMER DETAILS" and "CUSTOMER LOCATION." This improves query speed and efficiency while also streamlining data administration.
Carefully curating dimension tables to ensure that each one represents a distinct feature of the data was another aspect of normalization. For example, the 'SALES DATE' dimension table has date-related properties like 'Day Name', 'Day Number', 'Day_ID', and 'Date' that enable a thorough temporal processing of sales data.
The Star Schema's structured relationships make it easy for users to carry out sophisticated analytical queries. Customers' buying behavior, product profitability, sales performance over time, and regional sales patterns can all be examined by users. This is
11
made possible by the Star Schema's effective and user-friendly design, which not only makes it clear how various data points relate to one another but also makes cross-sectional analysis quite potent.
The model used for the European bike sales data makes it possible for Power BI to provide a strong analytical framework, guaranteeing that users can obtain a comprehensive understanding of the dataset and utilize it to inform strategic planning and decision-making. The BI project is well-positioned for sophisticated data exploration and visualization thanks to the development of a fact table, the identification of exact relationships, and the normalization of data.
12
Findings Based on Analysis and Evaluation
The Power BI dashboards use a variety of graphics, such as pie charts, bar charts, geographic heat maps, and more. The efficacy of these images in displaying sales data, client demographics, and regional performance, respectively, led to their selection.
Bikes, for example, are the most popular category with the biggest sales volume, as seen by the "Total Unit Sold by Sub_Category" pie chart on the Product Performance dashboard, which offers a quick visual overview of sales distribution across several product categories.
The Product Performance dashboard now features a new metric called "Profit Margin by Sub_Category," which was not discussed in the session. This metric informs strategic product focus by offering insightful information about each subcategory's profitability.
The DAX formulae are effective tools in the BI project that can be used to calculate, extract, and analyze data in the Power BI environment. Every formula is designed to address certain business inquiries and offer insights that are not immediately obvious from the raw data on its own.
Although it usually refers to an age field rather than an ID, the AVERAGE CUSTOMER AGE metric most likely determines the average age of consumers. This metric aids in comprehending the consumer base's demographic makeup.
The average cost of the products sold and the average price at which they are sold are two examples of the financial components of the sales that are shown by the AVG UNIT COST and AVG UNIT PRICE measurements. These measurements are essential for determining how well pricing schemes are working and for preserving profitability.
A crucial performance indicator known as PROFIT MARGIN assesses how well a business turns a profit for every dollar of revenue. A percentage that represents overall profitability is obtained by dividing the total profit by the entire revenue.
In order to go deeper, PROFIT MARGIN BY_STATE examines profit margin at the state level. By considering every single sale made inside a state using the iteration function SUMX, it provides a detailed picture of profitability across various geographic regions.
Because it compares sales volume to customer base diversity and shows how efficiently sales are divided across age groups, the SALES EFFICIENCY indicator may be especially instructive.
A key metric called TOP CUSTOMER_LOCATION BY_REVENUE is used to determine which location generates the most revenue. To identify the best-performing customer location, this measure uses MAX in conjunction with CALCULATE to weed out irrelevant factors.
13
A simple but important metric, TOTAL SALES BY COUNTRY compiles sales information at the national level to give an overview of the state of the market across several nations.
The dataset is improved by the addition of new computed columns such as ORDER_DAY and MONTHLY_ORDER, which add more temporal dimensions for analysis. Comparably, new metrics such as TOTAL SALES OVERTIME and TOTAL PROFIT BY PRODUCT enable the tracking of sales trends over time and the comprehensive assessment of product performance, respectively.
The data model is enhanced by these DAX formulae and calculated columns/measures, which makes the Power BI tool a more dynamic and perceptive analytical platform that can handle challenging business intelligence problems and promote data-driven decision-making.
The Power BI dashboard designs provide an extensive, interactive visual study of European bike sales from 2011 to 2016. Every dashboard offers comprehensive and in-depth insights while concentrating on a certain aspect of the organization. Below is a detailed explanation of each:
Sales Performance
Key Findings:
Total Revenue and Profit: A high overall performance is shown by the dashboard, which shows a total revenue of 28 million and a total profit of 11 million.
14
Unit Sales: With a total of 35K unit orders and an average unit order of 11.53, the sales volume is high with a reasonable purchase size.
Profit Margin: 38% is implied by the profit margin of 0.38, as indicated by the data. Although this is a healthy margin for retail, a more precise evaluation requires the industry benchmark background.
Product Performance: Ordering patterns are stable, with minor midweek surges, as indicated by the daily trend for total orders.
Monthly Revenue Trend: June is when revenue peaks and November and August are when it falls, showing a clear seasonal trend.
Sales by Sub-Category and Product Performance: The most common sub-category in terms of sales is bikes, which is followed by caps and helmets. Sport-100 helmets, water bottles, touring tire tubes, repair kits, and AWG logo caps are the top 5 products in terms of total earnings.
Insights:
Seasonal Variations: Monthly income shows a distinct seasonal variation that may be related to weather-related factors that impact cycling activity.
Product Popularity: The most popular categories are bikes and bike accessories, indicating that buyers are investing in accessories in addition to bikes, which may point to a loyal client base.
Profitable Items: Although bikes make up a large portion of sales, the most profitable products are water bottles and helmets, which may point to strong accessory margins.
Recommendations:
Stock management: Plan ahead and keep an eye on inventory levels to satisfy seasonal demand and guarantee a sufficient supply during the busiest months.
Target marketing initiatives to increase sales throughout the off-season. You may do this by holding events or promotions to entice customers to make purchases outside of the regular season.
Product Focus: Since accessories have large profit margins and the potential to raise average transaction value, think about broadening the selection of accessories supplied.
Customer Loyalty: Considering the steady ordering tendencies, it would be beneficial to establish or improve a customer loyalty program to promote recurring purchases.
15
Product Performance
Key Findings:
Profit Margin Analysis: The profit margins for different items are displayed in the bar chart. There are products with high margins and some with much lower margins, such as the 'Touring-3000 Blue, 62'.
Revenue Analysis: According to the 'Product Performance by Total Revenue' bar chart, 'Mountain-200 Black, 38' is the product that brings in the most money.
Top 5 Items by Total Sales: The top-earning products are from the 'Mountain-200' series, which appears to be a high-earning product line.
Poorest 5 Items in Terms of Total Revenue: Products with the lowest revenue performance include "Mountain-500 Black, 52" and "Mountain-100 Silver, 44."
Total Revenue by Product Type: The majority of overall profits (67.34%) are from bikes, with accessories coming in second (26.5%) and clothing third (6.16%).
Insights:
Product Focus: The revenue is dominated by the 'Mountain-200' series, indicating either higher pricing or greater popularity.
16
Profit vs. Revenue Differences: Due to high sales volume, several products with lower profit margins are nonetheless among the top revenue producers.
Underperformers: The goods that make up the 'worst 5' in terms of revenue may be costly or not attract enough customers.
Profits by Category: Bikes are the most profitable category, greatly outpacing Accessories and Clothes, which may point to the company's primary area of expertise.
Recommendations:
Product Strategy: Look into the low-margin items to see if there are any opportunities to cut expenses or modify price plans.
Sales Focus: In order to optimize income, marketing initiatives might concentrate on the 'Mountain-200' series, given its success.
Product Improvement or Discontinuation: Determine whether low-performing products should be discontinued to free up resources for higher-earning things, or whether they can be improved.
Diversify Your Offerings: Although bikes are the primary source of profit, think about ways to boost the revenue and profitability of clothing and accessories, maybe by selling them together with bikes.
Geography Analysis
17
Key Findings:
Top States by Revenue: With 11 million, England has the highest total revenue, followed by 2 million each by Hessen, Saarland, and Nordrhein-Westfalen.
Sales Efficiency: As seen by the pie chart, sales are distributed differently among the states, with England accounting for a sizeable portion of the total.
Total Unit Sold by Age Group and Country: The graph indicates that the greatest consumer segment worldwide is made up of adults (35–49).
State-wise Total Unit Sold: The distribution of unit sales by state is depicted in a map visualization, with a concentration in England and certain areas of Germany and France.
Total income by Subcategory and Customer Age: This shows the motorcycles that customers of different ages are buying, with adults once again generating a sizable amount of income.
Insights:
Market Concentration: The majority of revenue comes from England, which may be a sign of a robust market or advantageous market circumstances.
Customer Age Group: The majority of customers are adults (aged 35 to 49), which may be due to their greater discretionary spending or preference for bicycling.
Geographic Sales Distribution: As can be seen from the map, sales are not dispersed equally; some regions, such as England, and some portions of Germany and France, perform better than others.
Recommendations:
Market Expansion: Consider tactics to boost market share in states or regions that are underrepresented or have poorer sales efficiency.
Targeted Marketing: Since adults aged 35 to 49 make up the majority of buyers, concentrate marketing and sales efforts on this demographic. Adapt your messaging to their inclinations and purchasing patterns.
Localized Inventory Management: To guarantee that supply meets demand in high-revenue areas like England and avoid overstocking in lower-revenue regions, adjust inventory levels based on geographic sales performance.
18
Diversification: Despite the strength of the adult demographic, look for ways to reach out to younger and older audiences with tailored goods or advertising initiatives in order to broaden your clientele.
Customer Demography
Key Findings:
Revenue by Gender: At 17 million, the total revenue made by men is far more than that made by women (11 million).
Client by Age Group: According to the bar graph, the greatest client group is made up of adults (35–64), who are followed by young adults (25–34).
Customer Distribution by Gender and Age: The scatter plot indicates that the client base is spread widely throughout all age groups, with a concentration of male customers in all age ranges.
Revenue by Product and by Population: The overall profit by product, broken down by country and customer gender, is displayed in a horizontal stacked bar chart. It is evident that adult males (35–64) make up the largest portion of profit in both France and Germany.
Insights:
Gender-Based Revenue Gap: There is a discernible variation in the amount of money made depending on the gender, with male clients making larger contributions.
19
Dominant Customer Segment: Adult customers (ages 35 to 64) make up the majority of purchases; this may be due to their higher level of spending power or increased interest in bicycling.
Profitable Demographics: In all of the countries examined, male consumers—especially those who are adults—represent the most profitable group.
Recommendations:
Targeted Marketing to Women: Create plans to attract and convert more female consumers, whether by providing goods that suit their tastes or appealing to their emotions in advertising.
Retention of Core Customer Base: Make sure customer retention tactics, including loyalty programs or after-sales services, are in place as adults (35–64) make up the majority of the customer base.
Product and Service Diversification: Take into account the wide range of ages in your customer base and expand your product offerings to meet the diverse demands and preferences of these age groups.
Operational Insights
Key Findings:
20
Sales Efficiency and Profit Margin by State: The line graph shows that sales efficiency has significantly decreased throughout the states.
Revenue, Profit, and Unit Order Totals by Country: Germany leads in total profit, whereas the UK leads in total unit orders and total revenue.
Sales Efficiency and Total Revenue by State: There is a significant variation in sales efficiency across states. For example, England has a substantially higher efficiency than states like Scotland and Nordrhein-Westfalen.
Total Unit Sold and Sales Efficiency by client Age: A scatter plot illustrates how total units sold are distributed across different client ages, but it also suggests that sales efficiency declines with customer age.
Insights:
Concerns about Sales Efficiency: The dramatic drop in sales efficiency points to either operational problems or market saturation in some areas that require attention.
Performance of the Market by Nation: In terms of sales volume, the UK market seems to be the biggest, but Germany's market is the most lucrative.
Income versus Effectiveness: England exhibits great sales efficiency; however this does not always translate into the highest income, suggesting that efficiency by itself does not determine revenue.
Relationship between Customer Age: Although there is no direct correlation between younger clients and higher total unit sales and sales efficiency, this suggests that there may be room for improvement in sales processes.
Recommendations:
Operational Review: Look into why sales efficiency is dropping in different states and deal with any obstacles in the market or bottlenecks in operations.
Pay Attention to Profitability: Despite the UK market's large volume, pay attention to the tactics that have increased the profitability of the German market.
Sales Training and Procedures: Examine sales training and procedures to guarantee consistent and successful sales techniques, especially in light of the variation in sales efficiency, especially in England.
Age-Based Approaches: To increase sales efficiency for all age groups, create customized tactics that cater to their needs. For example, younger customers may benefit from a
21
concentration on digital channels, while elderly customers may benefit more from more traditional channels.
Every dashboard is thoughtfully designed to provide the most pertinent information in an understandable manner, facilitating quick analysis and decision-making. The dashboards make sure that stakeholders can rapidly understand the insights required to move the business ahead by using a combination of visual elements to tell the story of the data, from high-level financial overviews to in-depth demographic assessments.
Advanced Animated Power BI Chart
Key Findings:
1.
Product Performance: The 'Sport-100 Helmet, Red' appears to be the top-performing product in terms of total profit and revenue for the year displayed.
2.
Yearly Income Animation: The play axis suggests that there is a dynamic change in total income over the years, which can be used to observe trends and patterns over time.
22
3.
Seasonal Revenue Fluctuations: The monthly profit and revenue chart shows variations throughout the year, with some months like June and December having peaks, indicating potential seasonality in purchases.
Insights:
1.
Top Products: The animated bar chart race reveals that certain products consistently perform well, possibly due to popularity or seasonal buying habits.
2.
Trend Analysis: The animation of income over time can highlight important growth trends or periods of decline that correlate with external events or business initiatives.
3.
Seasonal Marketing Opportunities: The peaks in certain months suggest that there are specific times of the year when consumers are more likely to purchase, which could be leveraged for targeted marketing campaigns.
Recommendations:
1.
Focus on High-Performers: Increase marketing and stock for high-performing products like the 'Sport-100 Helmet, Red' to capitalize on their success.
2.
Expand Seasonal Strategies: Develop promotional strategies that align with the seasonal trends observed, such as special offers or advertising campaigns during peak months.
3.
Trend Monitoring: Utilize the play axis feature to continuously monitor changes in income over time, allowing for swift response to emerging trends or issues.
4.
Diversification: While focusing on top performers, also look for opportunities to diversify the product portfolio to mitigate risk in case of changing consumer preferences.
23
Conclusion and Recommendations:
After a thorough examination of the European bike sales data using the Power BI dashboards, we derive a number of useful conclusions and tactical suggestions, including:
Insights into sales performance: Consistent profit margins and a high volume of units sold point to a robust market presence. The erratic monthly revenue, however, points to a need for stronger sales consistency.
Product Performance: Key Information The sales and profit domination of specific bike subcategories indicates that inventories and marketing strategies should concentrate on these. The information also shows how pricing tactics might be improved to increase profitability.
Insights from Geographic Analysis: The sales heatmap illustrates which regions have considerable market penetration. To establish a more balanced market presence, there is a chance to repeat successful techniques in underperforming regions.
Customer Demographic Insights: Age and gender segments that could be more successfully targeted are revealed by customer purchase patterns. Tailoring marketing techniques to these groups is crucial in order to optimize engagement and sales.
Operational Insight: The relationship between profit margin and sales efficiency by state suggests that enhancing operations in particular areas may have a positive impact on the bottom line.
Recommendations:
Target High-Performance Products: To build on the current market performance of the bike subcategories that are performing well, increase marketing and stock for those models.
Enhance Pricing Strategy: Examine a product's price elasticity and modify pricing models to increase margins when feasible without sacrificing competitive positioning.
Regional Sales Strategy: To gain market share, use effective sales techniques from high-performing regions to lower-performing ones.
Demographic-Focused Marketing: To improve client acquisition and retention, create focused marketing efforts that appeal to the primary demographic groupings, such as youngsters or particular gender divisions.
Operational Efficiency Improvements: To find and fix operational bottlenecks and increase profit margins, concentrate on areas with low sales efficiency.
24
Implementing consumer Relationship Management (CRM): To better track consumer preferences, enhance service, and personalize marketing initiatives, implement or upgrade CRM systems.
Data-Driven Culture: Encourage a culture where decision-making is regularly based on BI tools, and make sure that all organizational levels are aware of and able to make use of the insights that Power BI dashboards offer.
Although the current sales performance is impressive, strategic initiatives with a specific focus could lead to a considerable increase in sales. The company may improve customer value, bolster its market position, and streamline processes by utilizing the insights from these BI technologies.
