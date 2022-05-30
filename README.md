1. Link：[Kaggle](https://www.kaggle.com/datasets/anmolkumar/health-insurance-cross-sell-prediction)

2. Competition name：health insurance cross sell prediction

3. Strategy Suggestion:
    - [X] enhance ensemble model -> most of ensemble models shows better predictions
    - [ ] build customized model -> EX：stacking...
    - [ ] adjust model params -> some model can adjust loss_func. etc...
    - [X] try under sampling methods -> random pick same number of positive samples
    - [X] add scaler -> EX：minmaxscaler, standardscaler...
    - [ ] feature engineering -> pca, lda, z-score picking...
    - [ ] clustering first
4. To-Do-List
    - [X] add annotations -> EX：plots should have insights, coding meanings & purpose...
    - [X] produce an output coding & CSV(best roc_auc one)
5. Experimental results
    
    **Decanter AI**
    | Model | Name | Cross-Validation | Hold-Out |
    | ----------- | ----------- | ----------- | ----------- |
    | Best | Random Forest | 0.9383 | 0.8467 |
    | Recommend | Gradient Boosting Machine | 0.8700 | 0.8517 |
    **BEST**
    - ROC-AUC：99.9%
    - important feature：Previously_Insured
    - Process：
      1. labelencoder -> Gender、 Vehicle_Damage、Vehicle_Age
      2. StandardScaler -> Annual_Premium、Vintage
      3. get_dummy -> Vehicle_Age、Region_Code、Policy_Sales_Channel
      4. imbalance(under_sampling) -> InstanceHardnessThreshold:LogisticRegression
      5. train_test_split -> 8:2
      6. XGBoost(random one) -> can show important features(?
      7. cross_validation -> NO ABNORMALITY DETECTED
      8. confusion_matrix -> NO ABNORMALITY DETECTED
      9. show important features -> Previously_Insured、Vehicle_Damage
      10. to_csv -> submit prediction(HAVE NO ANSWER)
