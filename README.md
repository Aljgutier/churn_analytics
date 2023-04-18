# <center>Churn Analytics</center>

## Broadband Service Customer Churn Risk Predictive Model
[Jupyter Notebook for analyzing and developing a churn risk predictive model](https://github.com/Aljgutier/churn_analytics/blob/main/churn_prediction_broadband.ipynb) for a Broadband Service. A typical use case for a churn risk score is to support of customer targeting to drive actions for churn reduction. The data is from [Sireesha Pulipati Data Storytelling with Google Looker Studio, ch 10, availble on Github](https://github.com/PacktPublishing/Data-Storytelling-with-Google-Data-Studio/blob/master/customer_churn_data.zip). The data includes 510124 rows, representing customer data from 27,605 customers, 24 months (2 years), In summary, the notebook does the the following:
* Loads, cleans, and transforms data in preparation for ML Feature Engineering
* Feature analysis and Feature Engineering including the use of histplots, correlations, and barplots. 
* Variable Deskew, Standardization, and Oversample with SMOTE due to the (imbalanced dataset), feature importance.
* ML Training with evaluation of 3 models - RF, XGB and lightGBM. The final model chosen is lightGBM due to its excellent predictive performance and superior computational performance.
* Excellent predicitive performance is obtained and is exemplified with an AUC score of 91.7%. Without the use of SMOTE the AUC obtained was at about 75%. 
* Churn probabilities are predicted for the last month of service corresponding to the year 2022, month 6.


<figure>
 <img alt="RFM Segmentation Dashboard" title="RFM Segmentation Dashboard" src="./images/broadband_customer_churn_risk.png" style="width:100%" >
 <figcaption><center>Figure 1. Churn Risk (probability)</center></figcaption>
 </figure>


