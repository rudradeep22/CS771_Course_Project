## CS771 experiment results
{d_size},{t_train},{t_map},{1 - acc0},{1 - acc1}
* **changing the loss hyperparameter in LinearSVC (hinge vs squared hinge)**  
Squared hinge : 63.0,0.685684643802233,0.005965822609141469,0.01990000000000003,0.0006999999999999229  
Hinge :         63.0,11.375974231003784,0.0069424661924131215,0.04483999999999999,0.0027000000000001467  
Hinge loss needs `dual = True` to function, and since `n_samples > n_features`, dual takes longer to train with lesser accuracy   
So, `squared_hinge` gives better results

* **setting C in LinearSVC and LogisticRegression to high/low/medium values**  
    In [here](./generate_graph.ipynb)
* **changing tol in LinearSVC and LogisticRegression to high/low/medium values**  
    In [here](./generate_graph.ipynb)
* **changing the penalty (regularization) hyperparameter in LinearSVC and Logisti-cRegression (l2 vs l1)**  
    Linearsvc & l2 : 63.0,0.5492382521973923,0.0032554659992456436,0.01990000000000003,0.0006999999999999229
    Linearsvc & l1 : 63.0,21.450329407199753,0.007451414596289396,0.01990000000000003,0.0016999999999999238
    LogisticReg & l2 : 63.0,1.39733530478552,0.00390670660417527,0.019100000000000117,0.0010999999999998789
    LogisticReg & l1 : Left running for 30 mins, still no output :(