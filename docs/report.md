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

The data source was combined through pandas dataframe function. The data types had objects that needed to converted to 
float and the date needed to be converrted to datatime in order data exploation to begin. 

## **Results of EDA**

![image](https://github.com/DATA-606-2023-FALL-MONDAY/Rius_Jonathan/assets/70355050/3628edbb-54e9-4010-924b-98cc88b6adfe)

A simple line graph is used to explore trends, annotations were made to explore the effect recessions had on indicators. As you can see gdp and unemployment  
were most affected by recessions. Sometimes the interest rate was effected, and inflation remained relatively stable. In some recessions a high interest rate 
was used to combat inflation, in others, a low interest rate was used to surge the economy. Deflation occured in two recessions but not the other. 

---

![image](https://github.com/DATA-606-2023-FALL-MONDAY/Rius_Jonathan/assets/70355050/5f4a0689-ae17-4102-b99c-262c40c69f2a)

Interest rate had the highest range of numbers, and inflation had the least. Values typically ranged from 0 to 5 except for unemployment 
which had values more concentrated between 5 and 10. Interest rates are more variable because they can be easily manipulated in order 
to aid the ecoonmy or to control inflation. GDP and unemployment have outliners that typically occur during recessions. 

--- 
![image](https://github.com/DATA-606-2023-FALL-MONDAY/Rius_Jonathan/assets/70355050/f8827dca-949e-4d51-a344-6c84a4a1904a)

Not a lot of notable correlations. Since inflation rate and interest rate has the highest correlation regression analysis will be run. In reality, 
the fed will increase interest rates when inflation is too high or low so this makes sense. GDP and inflation correlation also occurs in nature, 
but this shows a relatively moderate one. Many of economic theory suggests these correlation should be higher but the only significant one is 
interest rate and inflation. Surprising. 

---

## **Results of ML**

Arima Models and Other Predictive Models

ARIMA Model for Time Series Forecasting 


ARIMA stands for autoregressive integrated moving average model and is specified by three order parameters: (p, d, q).


Because there is a correlation between interest rate and inflation( the Fed will often raises interest rate to slow inflation) predictive models such as linear regression, random forest, and extra tree will be used. 

---
![image](https://github.com/DATA-606-2023-FALL-MONDAY/Rius_Jonathan/assets/70355050/10a83c1b-3e16-476c-ae23-eef3c28f46af)

The model has a means squared error of 2.22 which is pretty low and the forecast is realistic if no recessions occur. While the model does not take into account those recessions, the forecast of the percent

change going between 0 and 2.5 is a realistic one. This combined with a low MSE means its a decent model.

---
![image](https://github.com/DATA-606-2023-FALL-MONDAY/Rius_Jonathan/assets/70355050/bb0eec22-e72b-4735-956f-90613ee045ac)

This means squared error is almost 8 and the model is somewhat unrealistic. In a nature setting the interest rate changes according the economic landscape to induce or slow down borrowing.
This model shows an increase of the interest rate over many years and this just not economically feasible.

---

![image](https://github.com/DATA-606-2023-FALL-MONDAY/Rius_Jonathan/assets/70355050/6ea2202b-9e65-4760-b51b-fa7cb1d2b644)

This has a high means squared error of 24, the model is also highly questionable, if continued past ten years the unemployment is in the negatives. This is  impossible. The unemployment rate

changes greatly to economic contacting and recession like events. 

---
![image](https://github.com/DATA-606-2023-FALL-MONDAY/Rius_Jonathan/assets/70355050/0c0f6712-74b9-43ad-8fad-24105287bbb8) ![image](https://github.com/DATA-606-2023-FALL-MONDAY/Rius_Jonathan/assets/70355050/5ea767ac-2c70-43e9-9344-e55b13235eba)

To put it briefly there was a correlation between the interest rate and inflation, a model was produced. The model has R2 of .47, so the model is adequate but not strong enough for

the interest rate to predict the target variable of inflation.  
---
## **Conclusion and Further research**

Let’s split the conclusion into several categories. 

Trends: Basic exploratory analysis reveals that recessions cause certain indicators to fluctuate and data going high or low is a result of outside economic forces. 

Frequency: Indicators showed most data was concentrated between values zero and five, except for unemployment rate. Inflation had the shortest range and interest rate had the highest range (thats because its easier to change). 

Correlations: Only one correlation (inflation vs interest rate) was above .5. In many economic situations the interest rate is used to control inflation. It was as a predictor variable for regression analysis. 

Arima modeling: All models besides the gdp will unrealistic, the gdp is the only plausible scenario (if recessions occur). 

Regression analysis: With interest rate as the predictor variable and the inflation as the target variable, the model’s R2 score was too low to be considered good. Therefore the interest rate does not necessarily predict inflation.

Further research: 

## **References**

https://www.investopedia.com/articles/personal-finance/020215/top-ten-us-economic-indicators.asp

https://www.investopedia.com/terms/f/federalfundsrate.asp

https://www.investopedia.com/terms/u/unemploymentrate.asp

https://www.clevelandfed.org/center-for-inflation-research/inflation-101/why-does-the-fed-care-start

https://www.investopedia.com/ask/answers/112814/why-does-inflation-increase-gdp-growth.asp#:~:text=GDP%20is%20the%20monetary%20value,demand%20and%2For%20reduced%20supply.


