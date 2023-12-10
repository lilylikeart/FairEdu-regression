# FairEdu-regression

**run_experiment.ipynb** contains codes to run the main experiments in the paper.

**fairness_evaluation.ipynb** provides codes to calculte the fairness metrics reported in the paper.
 
Best hyperparameters to obtain the reported results are as follows:
- Random Forests:
    - Numeracy: (max_depth=70,max_features='sqrt',min_samples_leaf=1, min_samples_split=3,n_estimators=1000,bootstrap=False)
    - Reading: (max_depth=100,max_features='auto',min_samples_leaf=2, min_samples_split=2,n_estimators=600,bootstrap=True)
    - Writing: (max_depth=80,max_features='sqrt',min_samples_leaf=1, min_samples_split=5,n_estimators=600,bootstrap=False)
- MLP:
    - Numeracy: (hidden_layer_sizes=(200,100),solver="lbfgs", activation="identity" ,alpha=0.0001,learning_rate='constant',random_state=42, max_iter=3000,early_stopping=True,n_iter_no_change=20)
    - Reading: (hidden_layer_sizes=(300,100),solver="lbfgs", activation="identity" ,alpha=0.01,learning_rate='constant',random_state=42, max_iter=3000,early_stopping=True,n_iter_no_change=20)
    - Writing: (hidden_layer_sizes=(500, 240, 120),solver="lbfgs", activation="identity" ,alpha=0.1,learning_rate='constant',random_state=42, max_iter=3000,early_stopping=True,n_iter_no_change=20)
- XGBoost:
    - Numeracy: (gamma=0.02,learning_rate=0.1,max_depth=8,min_child_weight=6,n_estimators=1000,colsample_bytree=0.7,subsample=0.4,reg_alpha=0.0001,reg_lambda=1,seed=42)
    - Reading: (gamma=0.01,learning_rate=0.1,max_depth=12,min_child_weight=12,n_estimators=1000,colsample_bytree=0.4,subsample=0.8,reg_alpha=0.0001, reg_lambda=1,seed=42)
    - Writing: (gamma=0.02,learning_rate=0.1,max_depth=4,min_child_weight=10,n_estimators=1000,colsample_bytree=0.8,subsample=0.7,reg_alpha=0.01, reg_lambda=1,seed=42)
 
More training details can be found in [this document](bit.ly/45acPfT).

Feel free to contact me(lin.li@monash.edu) if you have any questions.
