# Crowdfunding-Data-Analysis
Crowdfunding Data Analysis This repository contains an analysis of crowdfunding data using Power BI, SQL, Excel, and Tableau. It covers data processing, modeling, and key insights, including project success rates, funding trends, and KPIs. The analysis is based on datasets from Kickstarter and other platforms.

What is Crowdfunding?

Crowdfunding is a method of raising capital through the collective effort of individuals, typically via online platforms. It allows entrepreneurs, startups, and creative projects to receive financial support from a large number of people rather than relying on traditional investors. This approach has gained popularity due to its accessibility and ability to reach a global audience. Crowdfunding campaigns are commonly hosted on platforms like Kickstarter, Indiegogo, and GoFundMe.
Refer to the Kickstarter PDF for more information on crowdfunding.

Data Processing and Analysis

We have used the datasets provided in the folder. The data modeling process involved matching common columns across different datasets. After modeling the data, we utilized it to answer the questions listed below using four different tools: Power BI, SQL, Excel, and Tableau.

Analysis Questions

1. Convert the Date Fields to Natural Time
The dataset contains dates in Epoch time format.
Refer to the attached article for Epoch Time conversion: Epoch Time Converter.

2. Build a Calendar Table Using the Created Date Column
The table should span from the minimum date to the maximum date.
Add the following columns using formulas:
Year
Month Number
Month Full Name
Quarter (Q1, Q2, Q3, Q4)
Year-Month (YYYY-MMM)
Weekday Number
Weekday Name
Financial Month (April = FM1, May = FM2, ..., March = FM12)
Financial Quarter (Quarters based on Financial Month: FQ-1, FQ-2, etc.)

3. Build the Data Model
Utilize the attached Excel files to structure the data model.

4. Convert the Goal Amount into USD
Convert the Goal column using a static USD rate.

5. Projects Overview KPIs
Total number of projects based on outcome
Total number of projects based on location
Total number of projects based on category
Total number of projects created by year, quarter, and month

6. Successful Projects
Total amount raised
Number of backers
Average number of days for successful projects

7. Top Successful Projects
Based on the number of backers
Based on the amount raised

8. Percentage of Successful Projects
Overall success percentage
Success percentage by category
Success percentage by year and month
Success percentage by goal range (ranges defined as per requirements)

Steps for Specific Questions

Q1) Converting Epoch Time to DateTime
Transforming Data - First 200,005 rows
Epoch time is in seconds; convert it using the formula:
#datetime(1970,1,1,0,0,0) + #duration(0,0,0,[EpochColumn])

-The main column in the dataset is created_at.
-Change the data type to Date/Time and load the data.
-Handle null values – blank columns appear after loading.

Q2) Creating a Calendar Table
Using Power Query Editor (PQE):
Calculate minimum and maximum dates using:
MIN(H:H)
MAX(H:H)

Use the Advanced Editor in Power Query to:
-Define created_at as the main column for min/max dates.
-Add required date-related columns with appropriate data types.

Q4) Converting Goal Amount to USD
-Transform the [goal] column to a decimal number or currency.
-Create a new parameter USD_Rate (Static USD Rate: 1 assumed).
-Create a new column Goal_USD with the formula:
[goal] * USD_Rate
Change the data type to decimal number.

Tools Used
1) Power BI
2) SQL
3) Excel
4) Tableau
