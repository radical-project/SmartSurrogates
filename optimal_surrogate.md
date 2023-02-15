Problem statement - The aim is to find the optimal point at which there is a right balance between the accuracy and the compute costs of the model.

Towards this we need to define a function that can be optimised.

Different Surrogate modelling techniques

- ALAMO
- ANNs
- GP regression
- MARS
- RF
- SVM regression
- There are more to survey

Factors that can be considered for creating a Optimizing function

- To analyze and compare the models, we need to check the
  - surface of the gradient - need to do surface approximation of various models - can it be thought in terms of number of local minima present beyond a certain number.
  - accuracy - can be measured using various metrics. Therefore need to identify those that can be used in an optimization function.
  - cost of training - in terms of time of $$ ?
  - metrics for higher scale??
  - what can be an ideal ratio between the relative accuracies of models and comppute costs? - need to calculate in case of scientific machine learning.
  -
