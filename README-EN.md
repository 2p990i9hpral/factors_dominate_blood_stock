# Documents

### [Paper](<How is Korea’s Blood Supply Maintained.pdf>)

# Summary

1.  Identified factors influencing blood supply and demand through EDA and domain knowledge.
2.  Collected and preprocessed unstructured data from various sources.
3.  Modeled blood supply and demand during crisis situations using time-series analysis methodologies.
4.  Visualized analysis results and proposed strategies for more efficient promotional campaigns.

## Findings

-   Quantitatively measured the impact of external factors on blood supply and demand.
-   Verified the effectiveness of the "Crisis-Level Blood Supply Response Plan" (which aims to increase supply and reduce usage during crises).
-   Quantitatively measured the effectiveness of promotions based on blood donor characteristics.

# Source Codes
- [EDA of Yearly Data](analysis_main.ipynb)
- [Comprehensive Data Analysis (EDA/Modeling/Visualization)](analysis_main.ipynb)

# Project Details

## Data Collection and Preprocessing

Identified factors influencing blood supply and demand based on domain knowledge gained through EDA, then collected relevant data.

### General Promotion Data

> ![](<images/Pasted%20image%2020250401223136.png>)
> Original raw data (before preprocessing).

> ![](<images/Pasted%20image%2020250401223201.png>)
> Data preprocessed using Python and Pandas.

Transformed raw data from report formats into a tabular data structure.

### Special Promotion Data

> ![](<images/Pasted%20image%2020250401223307.png>)
> Special promotion data as found on the web.

> ![](<images/Pasted%20image%2020250401223333.png>)
> Data collected and cleansed using Python and Selenium.

Scraped special promotion data from the web and preprocessed it into a tabular format.

### Donor Count Data

> ![](<images/Pasted%20image%2020250401231516.png>)
> Original raw data (before preprocessing).

Converted original Excel data into Pandas DataFrames and preprocessed it (e.g., handling missing dates, imputation) using scikit-learn and NumPy.

## EDA (Exploratory Data Analysis)

Identified external factors influencing blood data through EDA.

> ![](<images/Pasted%20image%2020250401223452.png>)
> Observed differences in donor count distributions by day of the week and holidays.

> ![](<images/Pasted%20image%2020250401223837.png>)
> Assessed the impact of the day of the week on the overall donor count distribution.

> ![](<images/Pasted%20image%2020250401223926.png>)
> Assessed the impact of holidays on the overall donor count distribution.

> ![](<images/Pasted%20image%2020250401224145.png>)
> Observed differences in monthly donor count distributions.

> ![](<images/Pasted%20image%2020250401224252.png>)
> Confirmed the significance of the precipitation variable.

> ![](<images/Pasted%20image%2020250401224750.png>)
> Examined blood inventory status during the COVID-19 period (confirming the significance of 'COVID period' and 'blood shortage period' variables).

## Modeling

Modeled blood supply and usage by region and gender, controlling for external factors.

> ![](<images/Pasted%20image%2020250401225310.png>)
> ![](<images/Pasted%20image%2020250401225322.png>)
> Captured annual seasonality in the data using Fourier terms, which were then used as control variables.

> ![](<images/Pasted%20image%2020250401224942.png>)
> ![](<images/Pasted%20image%2020250401225408.png>)
> Established a regression model including control variables\* identified as significant through EDA.
> (\* Variables: Day of the week, holidays, blood shortage period, COVID-19 period, Fourier terms for annual seasonality, precipitation, promotion period)

## Conclusion

Based on the model, measured changes during crisis situations and the effectiveness of promotions, then proposed strategies to enhance efficiency.

> ![](<images/Pasted%20image%2020250401221914.png>)
> Estimated regression coefficients for the blood supply model.

> ![](<images/Pasted%20image%2020250401225739.png>)
> Estimated regression coefficients for the blood usage model.

Confirmed that 'day of the week' and 'holiday' variables significantly impact both blood usage and supply.
Identified that COVID-19 reduced both blood usage and supply, with a more pronounced decrease in supply.
Verified that during blood shortage periods, blood usage decreases while supply increases.

> ![](<images/Pasted%20image%2020250401221531.png>)
> ![](<images/Pasted%20image%2020250401230429.png>)
> Promotion effectiveness by region and gender.

Quantitatively confirmed that promotions increased donor counts across all regional and gender groups, although the extent of the increase varied.

> ![](<images/Pasted%20image%2020250403210100.png>)
> ![](<images/Pasted%20image%2020250401230528.png>)
> Effectiveness of the sports ticket giveaway promotion.
> (Among special local promotions, sports ticket giveaways resulted in the highest percentage increase in donor counts.)

Confirmed that among various special promotions, the sports ticket giveaway was particularly effective compared to other methods.