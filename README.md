# credit-risk-classification

Logistic regression analysis of loans 


## Overview

The python notebook `credit_risk_classification.ipynb` contains the analysis, which entails a logistic regression for the classification of likely delinquent/troubled loans. A logistic regression is appropriate due to the binary nature of the dependant variable and desire for explainability in an underwriting context.  

## Model results

```
              precision    recall  f1-score   support

           0     0.9969    0.9950    0.9960     15001
           1     0.8601    0.9093    0.8840       507

    accuracy                         0.9922     15508
   macro avg     0.9285    0.9521    0.9400     15508
weighted avg     0.9925    0.9922    0.9923     15508
```

## Interpretation

The model retrieves more than 99% of healthy loans and about 91% of the risky loans. 9% of the at-risk loans it accordingly failed to detect. As the accurate detection of high-risk loans would be significantly more important in an underwriting context, and given that the latter make up a much larger part of the data, the general accuracy results and averages oversell the predictive utility of the model for its desired use case. A model tuned to this use case would permit lower precision for detecting risky loans in favor of improving this 91% recall rate.

In addition, very high multicollinearity is present which may make the model unstable and difficult to accurately characterise, inhibiting interpretability.

The recommendation would be to not use the model given these reservations and to use an approach that better incorporates the asymmetric nature of the problem.


## Disclaimer

No external code or other content has been used in this project, except where specifically provided in the assignment resources.
