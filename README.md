# Business-Insights-360-Case-Study

Welcome to the business insights 360 data analysis case study as a part of "Get Job Ready: Power BI Data Analytics for All Levels 2.0".

This project aims to build an automated POWER BI dashboard that would help the Finance, Sales, Marketing and Supply Chain team of AtliQ Hardware in order to effectively analyze the data and drive business insights to incorporate data-powered decisions. 


# Problem Statement 
AtliQ Hardware (a hypothetical company) faces challenges in effectively using and gaining insights from their data. They rely on old excel files to analyze their data but this method is outdated and not helpful in generating meaningful insights. This makes it hard for the company to grow fast and deal with problems in different countries. They lost a lot of money in Latin America because they did not have a solid system to analyze their data. They need to change from using excel to a new robust system that can analyze their data better. This new system should be able to handle high volume of data, be easy for people to use and give them organized information in order to make decisions. By solving this problem, AtliQ Hardware can enhance operational efficiency, avoid potential losses and get more business in all the countries. Using a modern data analytics system will help them grow and make more profits.

# About Dataset
The data used by AtliQ Hardware consists of a variety of information related to their operations, sales, customer demographics and market trends. It includes data from different countries where the company operates, allowing for a comprehensive understading of their business performance and market dynamics. The dataset is diverse and extensive which covers wide variety of segments such as product sales, regional market trends, customer preferences and financial information.

# Business requirement
 Following tasks need to be peformed to design the required dashboard : 
1. Finance View : Metrics, P & L table structure, Last year calculations, Quarters & YTD/YTG slicer, Dynamic switch on P & L table between targets and last year, Performance chart, top product/market/region visual.
  
2. Sales View :  Performance matrix visual, Toggle button to switch between visuals, Customer & Product performance chart, Unit Economics visuals.
   
3. Marketing View :  Performance matrix visual, Tooltip to represent trends, Product performance chart, Region/market/product performance chart.
   
4. Supply Chain View :  Key metrics by product and customer visual, accuracy/net error trend chart.
   
5. Executive View :  KPI's such as net sales, gross margin %, net profit % and forecast accuracy %, Market share visual, Revenue by division & channel visual.

# Production Grade BI 360 Dashbord
Click below to experience live dashboard
- [Power BI Dashboard](https://app.powerbi.com/view?r=eyJrIjoiZDEwMmExYmItN2VlNy00ZDJlLWI0ZGUtNjcyMjY1OTZmNmY5IiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9 ).


# Methodology

**Step 1:** To get started, I used MySQL Workbench's SQL queries to first explore the data. After a quick review of the data, these are my preliminary inferences:
1.  The database comprises 13 tables sourced from MySQL and external Excel files, categorized into fact tables with quantitative sales-related data and dimension tables providing customer, product, and market details.

2.  Dimension tables include information on 27 markets, 73 products across 14 categories, and 74 unique customers globally. Atliq's observation period for sales transactions and forecasts spans from September 2017 to August 2022, aligned with its fiscal year running from September to August.

3.  The transaction data is in INR and encompasses various metrics such as sales transaction details, forecast information, gross price, manufacturing cost, freight cost, and pre & post invoice deductions. The product lineup is organized into three major divisions and six segments, reflecting a comprehensive overview of Atliq's business landscape.

**Step 2:** I initiated the **ETL(Extract, Transform, Load)** procedure after obtaining a basic grasp of the data. My discoveries:
1. The dataset analysis revealed that all columns, except for the "region" column in the dim_market dataset, were free of errors and empty values.

2. In the absence of a date dimension table, a new one named dim_date was created in Power Query. This table was populated with calculated columns for fiscal year computation, utilizing dates from the fact_forecast_monthly and fact_sales_monthly datasets as references

**Step 3:** Once the first transformations were finished, I loaded the cleaned data into the main report. I began the next step of data modeling, which lays the groundwork for a strong analytical framework.


![image](https://github.com/bala942/BI-360-project/assets/127521506/2bfb7691-8f26-4d9c-aee2-138f8507040b)

                                                   Snow flake Schema

**Step 4:** The data validation phase followed, during which the project owner provided me with benchmark numbers. After comparing my data to these standards, I noticed something:

1. Identified a discrepancy of 376K in the total forecast quantity during the analysis.
2. Collaborated swiftly with the data engineering team to pinpoint and rectify the underlying data quality issue.


**Step 5:** The last phase involved optimizing the dashboard's performance. Using DAX Studio, I refined the dashboard, resulting in an impressive 30% reduction in file size and considerably faster data loading. This enhancement ensures a smooth user experience, improving the efficiency of exploring and visualizing data.


**Step 6:** I started the dashboard design process after making sure my data was ready and clean. This required creating the remaining calculated columns and measures, making use of DAX's (Data Analysis Expressions) capabilities, and creating the graphics required to accomplish a smooth combination of informative data and eye-catching design.

# Different View's

                                                       Home View
![Screenshot 2024-03-06 161534](https://github.com/bala942/BI-360-project/assets/127521506/a64036b9-8d07-4c08-8ab0-c2b31243b092)

                                                   Home view support on
![Screenshot 2024-03-06 162047](https://github.com/bala942/BI-360-project/assets/127521506/caa135d6-89f7-43ab-acdc-0425b019cde8)

                                                 Home view information on 
![Screenshot 2024-03-06 162028](https://github.com/bala942/BI-360-project/assets/127521506/eae339f6-a385-4b4e-9bc3-7f33449baf8f)
                                                     
                                                     AtliQ Map view
![Screenshot 2024-03-06 161553](https://github.com/bala942/BI-360-project/assets/127521506/e2d0ba68-f6a2-4f6e-acac-ba50d25d35c3)

                                               finance view in switch panel
![Screenshot 2024-03-06 161605](https://github.com/bala942/BI-360-project/assets/127521506/8028b1b3-64a0-441d-9c77-aa4caf8d74f0)

                                               finance view in filter panel
![Screenshot 2024-03-06 162112](https://github.com/bala942/BI-360-project/assets/127521506/0ffcc5d6-ca7d-4f36-a6cd-375b1941bfe1)
                                                    
                                              finance view in full view panel 
![Screenshot 2024-03-06 162138](https://github.com/bala942/BI-360-project/assets/127521506/d59c92b7-8a73-4c3f-814d-a08f9c25c1a6)
                                                       
                                                       Sales view
![Screenshot 2024-03-06 161703](https://github.com/bala942/BI-360-project/assets/127521506/2f623eee-e4e9-422a-aeeb-10f504027407)

                                               Sales view tool tip on visual
![Screenshot 2024-03-06 153934](https://github.com/bala942/BI-360-project/assets/127521506/ef1d35d9-3aae-491a-855f-8cd513a8e639)

                                                     Marketing view
![Screenshot 2024-03-06 161726](https://github.com/bala942/BI-360-project/assets/127521506/b6475322-0135-45fa-ac7c-e0a3a946f08e)
                                                              
                                                    Supply Chain view  
![Screenshot 2024-03-06 161750](https://github.com/bala942/BI-360-project/assets/127521506/3cfdcf7b-8f58-47e8-86be-41e7d5342051)

                                                      Executive view
![Screenshot 2024-03-06 161803](https://github.com/bala942/BI-360-project/assets/127521506/4c4466d4-8a5f-49c0-9c6c-ed521f1c43b9)
                                                              
                                                              
                                                          



I hope this project helps you understand the business insights. If you have any questions or suggestions, please don't hesitate to reach out.  
- [LinkedIn](https://www.linkedin.com/in/balacdatascientist)  
