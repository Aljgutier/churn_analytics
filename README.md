# <center>Churn Analytics</center>

## Broadband Service Customer Churn Risk Predictive Model
[Jupyter Notebook for analyzing and developing a churn risk predictive model](https://github.com/Aljgutier/churn_analytics/blob/main/churn_prediction_broadband.ipynb) for a Broadband Service. A typical use case for a churn risk score is to support of customer targeting to drive actions for churn reduction. The data is from [Sireesha Pulipati Data Storytelling with Google Looker Studio, ch 10, availble on Github](https://github.com/PacktPublishing/Data-Storytelling-with-Google-Data-Studio/blob/master/customer_churn_data.zip). The data includes 510124 rows, representing customer data from 27,605 customers, 24 months (2 years), In summary, the notebook does the the following:
* Loads, cleans, and transforms data in preparation for ML Feature Engineering
* Feature analysis and Feature Engineering including the use of histplots, correlations, and barplots. 
* Variable Deskew, Standardization, oversampling with SMOTE due to the (imbalanced dataset), and feature importance
* ML Training with evaluation of 3 models - RF, XGB and lightGBM. The final model chosen is lightGBM due to its excellent predictive performance and superior computational performance.
* Excellent predicitive performance is obtained and is exemplified with an AUC score of 91.7%. Without the use of SMOTE the AUC obtained was at about 75%. Recall and Selectivigy are as follows: sensitivity_recall_tpr = 0.854, specicifity_selectivity_tnr = 0.98
* Churn probabilities are predicted for the last month of service corresponding to the year 2022, month 6.


<figure>
 <img alt="RFM Segmentation Dashboard" title="RFM Segmentation Dashboard" src="./images/broadband_customer_churn_risk.png" style="width:100%" >
 <figcaption><center>Figure 1. Churn Risk (probability)</center></figcaption>
 </figure>


<figure>
 <img alt="ROC Curve" title=ROC Curve" src="./images/broadband_churn_prediction_roc_curve.png" style="width:100%" >
 <figcaption><center>Figure 2. Broadband Churn Prediction ROC Curve</center></figcaption>
 </figure>

# Broadband Service Churn BI

* Data - the data source is the same as for the above notebook. Two tables are are input to Big Query (Broandband Service Churn and Broadband Service Churn Prediction) and a single view is created for use by the dashboard. 
* 