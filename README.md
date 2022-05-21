1. Link：[Kaggle](https://www.kaggle.com/datasets/anmolkumar/health-insurance-cross-sell-prediction)

2. Competition name：health insurance cross sell prediction

3. Strategy Suggestion:
    - [ ] enhance ensemble model -> most of ensemble models shows better predictions
    - [ ] build customized model -> EX：stacking...
    - [ ] adjust model params -> some model can adjust loss_func. etc...
    - [ ] try under sampling methods -> random pick same number of positive samples
    - [ ] add scaler -> EX：minmaxscaler, standardscaler...
    - [ ] feature engineering -> pca, lda, z-score picking...
    - [ ] clustering first
4. To-Do-List
    - [ ] add annotations -> EX：plots should have insights, coding meanings & purpose...
    - [ ] produce an output coding & CSV(best roc_auc one)
5. Experimental results
    
    **Decanter AI**
    | Model | Name | Cross-Validation | Hold-Out |
    | ----------- | ----------- | ----------- | ----------- |
    | Best | Random Forest | 0.9383 | 0.8467 |
    | Recommend | Gradient Boosting Machine | 0.8700 | 0.8517 |
