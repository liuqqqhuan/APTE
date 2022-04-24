# APTE
This is our Tensorflow implementation for our APTE paper and a part of baselines:

>APTE: Adaptive Preference Transfer for Personalized IoT Entity Recommendation.

## Environment Requirement
The code has been tested running under Python 3.8.0. The required packages are as follows:
* tensorflow == 1.14.0
* numpy == 1.16.4
* scipy == 1.3.1
* pandas == 0.17

## C++ evaluator(换成运行的步骤)
We have implemented C++ code to output metrics during and after training, which is much more efficient than python evaluator. It needs to be compiled first using the following command. 
```
python setup.py build_ext --inplace
```
If the compilation is successful, the evaluator of cpp implementation will be called automatically.
Otherwise, the evaluator of python implementation will be called.

## Examples to run APTE:
run [main.py](./main.py) in IDE or with command line:
```
python main.py
```

NOTE :   
(1) the duration of training and testing depends on the running environment.  
(2) set model hyperparameters on .\conf\APTE.properties  
(3) set NeuRec parameters on .\NeuRec.properties  
(4) the log file save at .\log\yelp_gat\  

## Dataset
We provide Yelp dataset.
  * .\dataset\yelp_gat.rating and yelp.uu
  *  Each line is a user with her/his positive interactions with items: userID \ itemID \ ratings .
  *  Each user has more than 10 associated actions.

