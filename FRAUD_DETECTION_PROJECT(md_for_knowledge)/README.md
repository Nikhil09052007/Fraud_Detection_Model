## This specific section contains all the theoritical knowledge which is required for this project.

# Below is the structure for the context:
FRAUD_DETECTION_RISK_SCORING/
│
├── README.md
│
├── 01_FINANCIAL_WORLD/
│   ├── README.md
│   ├── What_is_Money.md
│   ├── What_is_a_Financial_Transaction.md
│   ├── What_is_a_Bank.md
│   ├── What_is_Fintech.md
│   ├── What_is_an_Account.md
│   ├── What_is_a_Card.md
│   └── What_is_a_Merchant.md
│
├── 02_PAYMENT_ECOSYSTEM/
│   ├── README.md
│   ├── Customer.md
│   ├── Merchant.md
│   ├── Payment_Gateway.md
│   ├── Payment_Processor.md
│   ├── Acquiring_Bank.md
│   ├── Issuing_Bank.md
│   ├── Card_Network.md
│   └── How_Payment_Entities_Interact.md
│
├── 03_PAYMENT_LIFECYCLE/
│   ├── README.md
│   ├── Payment_Initiation.md
│   ├── Authentication.md
│   ├── Authorization.md
│   ├── Authentication_vs_Authorization.md
│   ├── Approval_and_Decline.md
│   ├── Clearing.md
│   ├── Settlement.md
│   └── Complete_Payment_Lifecycle.md
│
├── 04_FINANCIAL_FRAUD/
│   ├── README.md
│   ├── What_is_Financial_Fraud.md
│   ├── Who_is_a_Fraudster.md
│   ├── Fraudulent_vs_Legitimate_Transaction.md
│   ├── Fraud_vs_Theft.md
│   ├── Fraud_vs_Default.md
│   ├── Fraud_vs_Chargeback.md
│   └── Why_Fraud_is_Hard_to_Detect.md
│
├── 05_TYPES_OF_FRAUD/
│   ├── README.md
│   ├── Card_Fraud.md
│   ├── Card_Present_Fraud.md
│   ├── Card_Not_Present_Fraud.md
│   ├── Account_Takeover.md
│   ├── Identity_Fraud.md
│   ├── Synthetic_Identity_Fraud.md
│   ├── Payment_Fraud.md
│   ├── Application_Fraud.md
│   ├── Loan_Fraud.md
│   ├── Transaction_Fraud.md
│   └── Friendly_Fraud.md
│
├── 06_HOW_FRAUD_HAPPENS/
│   ├── README.md
│   ├── Stolen_Credentials.md
│   ├── Phishing_and_Social_Engineering.md
│   ├── Credential_Stuffing.md
│   ├── Data_Breaches.md
│   ├── Account_Takeover_Process.md
│   ├── Card_Testing.md
│   └── Fraud_Attack_Lifecycle.md
│
├── 07_TRANSACTION_ANATOMY/
│   ├── README.md
│   ├── Transaction_Amount.md
│   ├── Timestamp.md
│   ├── Customer_and_Account.md
│   ├── Merchant.md
│   ├── Payment_Method.md
│   ├── Device.md
│   ├── IP_and_Network.md
│   ├── Location.md
│   └── Transaction_History.md
│
├── 08_FRAUD_AS_DATA/
│   ├── README.md
│   ├── Real_World_to_Data.md
│   ├── Observable_vs_Unobservable_Information.md
│   ├── Transaction_Data.md
│   ├── Customer_Data.md
│   ├── Behavioral_Data.md
│   └── Fraud_Label.md
│
├── 09_NORMAL_VS_ABNORMAL_BEHAVIOR/
│   ├── README.md
│   ├── Normal_Behavior.md
│   ├── Abnormal_Behavior.md
│   ├── Behavioral_Deviation.md
│   ├── Transaction_Velocity.md
│   ├── Unusual_Amount.md
│   ├── Unusual_Time.md
│   ├── Unusual_Location.md
│   ├── New_Device.md
│   ├── New_Merchant.md
│   └── Multiple_Signals.md
│
├── 10_FRAUD_DETECTION/
│   ├── README.md
│   ├── What_is_Fraud_Detection.md
│   ├── Rule_Based_Detection.md
│   ├── Anomaly_Detection.md
│   ├── Manual_Review.md
│   ├── Risk_Based_Detection.md
│   ├── Machine_Learning_Detection.md
│   └── Hybrid_Fraud_Detection.md
│
├── 11_REAL_TIME_FRAUD_DETECTION/
│   ├── README.md
│   ├── Why_Real_Time_Matters.md
│   ├── Transaction_Arrival.md
│   ├── Real_Time_Feature_Generation.md
│   ├── Real_Time_Scoring.md
│   ├── Real_Time_Decision.md
│   └── End_to_End_Real_Time_Flow.md
│
├── 12_BUSINESS_PROBLEM/
│   ├── README.md
│   ├── Why_Companies_Care_About_Fraud.md
│   ├── Fraud_Loss.md
│   ├── False_Declines.md
│   ├── Customer_Experience.md
│   ├── Manual_Review_Cost.md
│   ├── Fraud_Prevention_Cost.md
│   └── Business_Tradeoffs.md
│
├── 13_DATA_SCIENCE_FORMULATION/
│   ├── README.md
│   ├── Business_to_ML_Problem.md
│   ├── What_Are_We_Predicting.md
│   ├── Target_Variable.md
│   ├── Features.md
│   ├── Labels.md
│   ├── Prediction_Point.md
│   └── Prediction_Horizon.md
│
├── 14_DATA_UNDERSTANDING/
│   ├── README.md
│   ├── Dataset_Overview.md
│   ├── Data_Dictionary.md
│   ├── Data_Types.md
│   ├── Missing_Data.md
│   ├── Duplicates.md
│   ├── Distributions.md
│   ├── Categorical_Data.md
│   ├── Numerical_Data.md
│   └── Exploratory_Data_Analysis.md
│
├── 15_FEATURE_ENGINEERING/
│   ├── README.md
│   ├── What_is_Feature_Engineering.md
│   ├── Transaction_Level_Features.md
│   ├── Customer_Behavior_Features.md
│   ├── Velocity_Features.md
│   ├── Time_Based_Features.md
│   ├── Location_Features.md
│   ├── Device_Features.md
│   └── Behavioral_Risk_Signals.md
│
├── 16_DATA_LEAKAGE_AND_TIME/
│   ├── README.md
│   ├── What_is_Data_Leakage.md
│   ├── Prediction_Time.md
│   ├── Information_Available_at_Prediction.md
│   ├── Future_Information.md
│   ├── Label_Leakage.md
│   ├── Train_Test_Leakage.md
│   └── Temporal_Data_Splitting.md
│
├── 17_CLASSIFICATION/
│   ├── README.md
│   ├── Classification_Problem.md
│   ├── Binary_Classification.md
│   ├── Logistic_Regression.md
│   ├── Decision_Trees.md
│   ├── Ensemble_Models.md
│   ├── Probability_Prediction.md
│   └── Classification_Threshold.md
│
├── 18_CLASS_IMBALANCE/
│   ├── README.md
│   ├── What_is_Class_Imbalance.md
│   ├── Why_Fraud_Data_is_Imbalanced.md
│   ├── Why_Accuracy_Can_Fail.md
│   ├── Resampling.md
│   ├── Class_Weights.md
│   ├── SMOTE.md
│   └── Cost_Sensitive_Learning.md
│
├── 19_MODEL_EVALUATION/
│   ├── README.md
│   ├── Confusion_Matrix.md
│   ├── True_Positive_and_Negative.md
│   ├── False_Positive_and_Negative.md
│   ├── Accuracy.md
│   ├── Precision.md
│   ├── Recall.md
│   ├── F1_Score.md
│   ├── ROC_AUC.md
│   ├── Precision_Recall_Curve.md
│   ├── PR_AUC.md
│   ├── Threshold_Evaluation.md
│   └── Cost_Based_Evaluation.md
│
├── 20_RISK_SCORING/
│   ├── README.md
│   ├── Probability_vs_Risk.md
│   ├── Risk_Score.md
│   ├── Score_Calibration.md
│   ├── Risk_Bands.md
│   └── Translating_Model_Output_to_Risk.md
│
├── 21_DECISION_ENGINE/
│   ├── README.md
│   ├── What_is_a_Decision_Engine.md
│   ├── Approval.md
│   ├── Manual_Review.md
│   ├── Blocking.md
│   ├── Decision_Thresholds.md
│   ├── Business_Rules.md
│   └── Model_plus_Rules.md
│
├── 22_EXPLAINABILITY/
│   ├── README.md
│   ├── Why_Explainability_Matters.md
│   ├── Global_vs_Local_Explanations.md
│   ├── Feature_Importance.md
│   ├── SHAP.md
│   └── Explaining_a_Fraud_Decision.md
│
├── 23_REAL_TIME_SYSTEM/
│   ├── README.md
│   ├── System_Architecture.md
│   ├── Data_Ingestion.md
│   ├── Feature_Pipeline.md
│   ├── Model_Serving.md
│   ├── API.md
│   ├── Decision_Service.md
│   └── End_to_End_System.md
│
├── 24_MONITORING/
│   ├── README.md
│   ├── Why_Monitoring_is_Necessary.md
│   ├── Data_Drift.md
│   ├── Concept_Drift.md
│   ├── Model_Performance_Monitoring.md
│   ├── Fraud_Rate_Monitoring.md
│   ├── False_Positive_Monitoring.md
│   └── Model_Retraining.md
│
├── 25_BUSINESS_EVALUATION/
│   ├── README.md
│   ├── Fraud_Prevented.md
│   ├── Financial_Loss.md
│   ├── Customer_Impact.md
│   ├── Review_Operations.md
│   ├── Model_ROI.md
│   └── Business_Success_Metrics.md
│
├── 26_COMPLETE_MENTAL_MODEL/
│   ├── README.md
│   ├── End_to_End_Fraud_System.md
│   ├── Connecting_All_Concepts.md
│   ├── Data_Scientist_Perspective.md
│   ├── System_Limitations.md
│   └── Interview_Mental_Model.md
│
├── data/
│   ├── raw/
│   ├── processed/
│   └── README.md
│
├── notebooks/
│   ├── 01_data_exploration/
│   ├── 02_feature_engineering/
│   ├── 03_modeling/
│   └── 04_evaluation/
│
├── src/
│   ├── data/
│   ├── features/
│   ├── models/
│   ├── scoring/
│   ├── decision/
│   └── monitoring/
│
├── app/
│
├── tests/
│
├── requirements.txt
│
└── .gitignore