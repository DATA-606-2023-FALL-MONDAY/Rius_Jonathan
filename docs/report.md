https://github.com/DATA-606-2023-FALL-MONDAY/Kandlagunta_Dheeraj/blob/main/docs/report.md



## **Title and Author**

Project Title: US Employment, Inflationm Interest Rate and GDP Exploration and Economic Forecasting

Prepared for UMBC Data Science Master Degree Capstone by Dr Chaojie (Jay) Wang

Author Name: Jonathan Rius

Fall 2023 Semester

Link to the author's GitHub profile https://github.com/jonnie763

Link to the author's LinkedIn profile https://www.linkedin.com/in/jonathan-rius-17612b207/

Link to your PowerPoint presentation file https://github.com/DATA-606-2023-FALL-MONDAY/Rius_Jonathan/blob/main/docs/Jonathan%20Rius_Final%20Presentation%20.pptx

Link to your YouTube video https://youtu.be/Oo_g2CpV0NM?si=nnLJqtQNIyDoQ7ek


## **Background**

**What are some macroeconomic metrics and why do they matter?**

There are many macroeconomic metrics but this project aims to investigate four metrics. This projects aims to investigate inflation,GDP percent change,
unemployment rate and federal interest rate. Why do economists put such emphasis on such figures? These indicators give social scientists a good indication
on the health of the economy. From here governments can take action and employ policy changes to improve these figures so that damage is mitgated. What 
do they do? They will generally increase government spending(like with unemployment insurance), lower taxes and regulations or will adjust the interest rate. 
In short, these metrics are some of the best infomation we have in gauging the health of the economy and using policy changes to fix holes in the economy.

How can one define each metric? *Inflation* (as measured in the project by CPI)  is the general price level rise of goods and services in an economy. 
Too much inflation can mean the economy is overheating while very low inflation can be a harbinger of economic recession. What about *GDP*? GDP stands
for gross domestic product (GDP),it  provides the overall value of the goods and services that the economy produces and indicates whether it is growing 
or slowing. The *Unemployment rate* is the percentage of the labor force without a job. *The federal interest rate*  refers to the target interest rate 
range set by the Federal Open Market Committee (FOMC).


**Research Questions**

What will inflation, GDP, unemployment rate and the federal interest look like in the future?

Can indicators predict the other (like with regression analysis)?

What are some correlations between economic indicators, and what are some trends that occur when looking at the data?

What is the frequency of most of the data? 

How economists use this data to make policy changes?


## **Description of Data Sources and Data Elements**

**Data Source**

The data uses several files to which they are combined. 

1. FEDFUNDS.csv
2. GDP (4).csv
3. CPIAUCSL (3).csv
4. UNEMPLOYMENT RATE.csv

**Data Size and Records**

The combined size of the files is 30 kb. The combined dataframe has 277 rows combined. 
The follwing data goes back to 1954 and ends in the year 2023. 

**Data Structure**

![image](https://github.com/DATA-606-2023-FALL-MONDAY/Rius_Jonathan/assets/70355050/b9bbe4db-99cf-44fa-9445-86973f2056d8)


## **Results of EDA**

![image](https://github.com/DATA-606-2023-FALL-MONDAY/Rius_Jonathan/assets/70355050/3628edbb-54e9-4010-924b-98cc88b6adfe)

A simple line graph is used to explore trends, annotations were made to explore the effect recessions had on indicators. As you can see gdp and unemployment  

were most affected by recessions. Sometimes the interest rate was effected, and inflation remained relatively stable.

![image](https://github.com/DATA-606-2023-FALL-MONDAY/Rius_Jonathan/assets/70355050/5f4a0689-ae17-4102-b99c-262c40c69f2a)

Interest rate had the highest range of numbers, and inflation had the least. Values typically ranged from 0 to 5 except for unemployment 
which had values more concentrated between 5 and 10. 

![image](https://github.com/DATA-606-2023-FALL-MONDAY/Rius_Jonathan/assets/70355050/8f7805e1-ad8b-4dbf-92c4-d46d84bb26b3) ![image](https://github.com/DATA-606-2023-FALL-MONDAY/Rius_Jonathan/assets/70355050/af55bdc0-5faa-4540-85f3-655df2c645c3)








## **Results of ML**

## **Conclusion and Further research**

## **References**

https://www.investopedia.com/articles/personal-finance/020215/top-ten-us-economic-indicators.asp

https://www.investopedia.com/terms/f/federalfundsrate.asp

https://www.investopedia.com/terms/u/unemploymentrate.asp
