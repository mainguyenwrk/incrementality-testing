**1. THE CHALLENGE**

The challenge was to identify the true impact of a nationwide new media campaign on overall revenue. The goal was to distinguish between correlation and actual causation, ensuring reliable conclusions regarding the campaign’s effectiveness.

**2. THE STRATEGY**
To address this challenge, I employed incrementality testing combined with correlation analysis. This involved using historical revenue data to assess the relationship between new media campaign spend and sales, ultimately determining if the campaign had a significant causal impact on revenue.

**3. THE PROCESS**

**Data Collection**: Gathered 01 years of weekly revenue data from Google Analytics.

**Correlation Analysis**: Conducted four Pearson’s correlation tests to examine the relationship between campaign spend and overall sales and engagement metrics.

  Revenue and Campaign Spend: Correlation of 0.0852, p-value: 0.5287 (indicating no significant relationship).
  
  Sessions and Campaign Spend: Correlation of -0.0312, p-value: 0.8179 (also indicating no significant relationship).
  
**Incrementality-testing:** As the media campaign is rolled out across the country, geo-experiments cannot be applied. Therefore, a synthesis control group approach is applied using time-series methods. 
    
    Baseline Forecasting: Developed two predictive models which are linear regression and Facebook Prophet to forecast revenue in the absence of the campaign, 
    selecting the best model based on adjusted R-squared and RMSE. Linear regression was as it has a higher Adjusted Rsquare and RMSE 
    as well as Adjusted Rsquare of 0.57 indicating a moderate fit which is acceptable from a stastical point of view:
    
    
                    Model	                Linear Regression 	      Prophet
                    Adjusted Rsquare	0.5714 (moderately fit)	  0.1944 (low fit) 
                    RMSE	                £188,315.59	              £249,947.11
    
    Incrementality Comparison: Compared observed revenue during the campaign with forecasted values to assess any significant differences.

**4. THE FINDINGS & INSIGHTS:**

Although the estimated cumulative incremental impact was £124,906.16, suggesting a potential additional ROAS of 6.05, the observed revenue did not significantly deviate from the predicted revenue. Together with the evidence from correlation analysis, this highlighted insufficient support for a significant causal impact on overall revenue. Thus, we concluded that there is insufficient evidence to support the hypothesis that the new media campaign has a significant causal impact on overall revenue.
![Screenshot 2024-07-14 at 00 03 18](https://github.com/user-attachments/assets/e9e7445c-6a16-4140-8b8c-87a4f529b213) ![Screenshot 2024-07-14 at 00 03 26](https://github.com/user-attachments/assets/1ff1b988-bf9e-400a-bae6-3894c87961b5)

**5. LEARNING & WISHES**:
- The test's duration was only for a month, which might affect the reliability of the result. Next time, it would be more ideal to aim for longer period of time to include more data for the model, ensuring confidence and enough data for possible trends/patterns discovered.
- To combine with Marketing Mix Modelling to identify and understand the Lagged effect of each type of campaign to identify the appropriate observed periods.
