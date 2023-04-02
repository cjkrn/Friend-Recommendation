# Facebook Friend Recommendation using graph mining


![image](https://drive.google.com/uc?export=view&id=1RW-TuP7bJY-dcURwCmx4MNHFgWB2uoiJ)


  
### Problem statement: 
Given a directed social graph, have to predict missing links to recommend users (Link Prediction in graph)

### Data Overview
Taken data from facebook's recruting challenge on kaggle https://www.kaggle.com/c/FacebookRecruiting  
data contains two columns source and destination eac edge in graph 
    - Data columns (total 2 columns):  
    - source_node         int64  
    - destination_node    int64  

### Mapping the problem into supervised learning problem:
- Generated training samples of good and bad links from given directed graph and for each link got some features like no of followers, is he followed back, page rank, katz score, adar index, some svd fetures of adj matrix, some weight features etc. and trained ml model based on these features to predict link. 

### Business objectives and constraints:  
- No low-latency requirement.
- Probability of prediction is useful to recommend ighest probability links

### Performance metric for supervised learning:  
- Both precision and recall is important so F1 score is good choice
- Confusion matrix

### Featurization techniques
- Jaccard distance
- Cosine distance (Otsuka-Ochiai coefficient)
- Page Rank
- Shortest path
- Connected Components
- Adar Index
- Does the person follow back?
- Katz Centrality
- Hits score
- Singular Value Decompostion
- Weight features
- Preferential Attachment (``ASSIGNMENT``)
- SVD_dot (``ASSIGNMENT``)
![image1](https://drive.google.com/uc?export=view&id=1u4fb0Za2v3_E2Hdw4G8w_MJVuzTxCJ4X)

### Models
- Random forest

    Confusion matrix with `TRAIN` data
    ![Random Train](https://github.com/cjkrn/Friend-Recommendation/blob/main/Final/Random%20Train%20Confusion%20Matrix.png)

    Confusion matrix with `TEST` data
    ![Random Test](https://github.com/cjkrn/Friend-Recommendation/blob/main/Final/Random%20Test%20Confusion%20Matrix.png)

- XGBOOST (``ASSIGNMENT``)

    Confusion matrix with `TRAIN` data
    ![XGBoost Train](https://github.com/cjkrn/Friend-Recommendation/blob/main/Final/XGBoost%20Train%20Confusion%20Matrix.png)

    Confusion matrix with `TEST` data
    ![XGBoost Test](https://github.com/cjkrn/Friend-Recommendation/blob/main/Final/XGBoost%20Test%20Confusion%20Matrix.png)

### Test result
![Results for Facebook Recommendation System](https://github.com/cjkrn/Friend-Recommendation/blob/main/Final/Facebook%20Friend%20Recommendation%20Results.png)


## Authors

- [Chiranjiv Karning] (https://www.linkedin.com/in/chiranjiv-karning/)
