# APTE
This is part of the code of our APTE method:

>APTE: Adaptive Preference Transfer for Personalized IoT Entity Recommendation.

## Environment Requirement
The code has been tested running under Python 3.6.0. The required packages are as follows:
* tensorflow-gpu == 1.14.0
* numpy == 1.19.5
* scipy == 1.2.1
* pandas == 1.1.5
* reckit == 0.2.4

## Simulation platform
* Intel@Core i9-10900K CPU
* NVIDIA GeForce RTX 2080Ti GPU
* Memory 64 GiB
* Ubuntu 18.04 LTS
* Pycharm Community
## Baseline method
* BPRMF: This is a ranking model which assumes that
users tend to assign higher scores to items that their friends prefer.
* NGCF: This is a recommendation framework based on graph neural network.
* EATNN: This is a adaptive transfer framework for social-aware recommendation.
* LGCN: This is a recommendation framework based on Simplifying and powering GCN.
## Examples to run APTE:
run main.py in IDE or with command line:
```
python main.py
```

## Parameter settings   
(1) the duration of training and testing depends on the running environment.  
(2) set model hyperparameters on ./conf/APTE.properties  
(3) set NeuRec parameters on ./Net.properties  
(4) the log file save at ./log/yelp_gat/  

## Dataset
We provide Epinions and Yelp dataset.
  * ./dataset/epinion.rating and epinion_gat.uu
  * ./dataset/yelp_gat.rating and yelp_gat.uu
  * Each line is a user with her/his positive interactions with items: userID \ itemID \ ratings .
  * Each user has more than 10 associated actions.

