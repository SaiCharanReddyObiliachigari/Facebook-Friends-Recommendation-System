# Facebook-Friends-Recommendation-System
Am going to approach the problem based on the path-lengths(edges) between two vertices(users).
Social network Graph Link Prediction - Facebook Challenge , Given a directed social graph, have to predict missing links to recommend users (Link Prediction in graph)
Data Overview: 
Taken data from facebook's recruting challenge on kaggle https://www.kaggle.com/c/FacebookRecruiting
data contains two columns source and destination eac edge in graph

- Data columns (total 2 columns):  
- source_node         int64  
- destination_node    int64
- Jacard Distance 𝑗=|𝑋∩𝑌|/|𝑋∪𝑌|
- 𝐶𝑜𝑠𝑖𝑛𝑒𝐷𝑖𝑠𝑡𝑎𝑛𝑐𝑒=|𝑋∩𝑌|/|𝑋|⋅|𝑌|
- Adamic/Adar measures is defined as inverted sum of degrees of common neighbours for given two vertices.
- 𝐴(𝑥,𝑦)=∑𝑢∈𝑁(𝑥)∩𝑁(𝑦)[1/𝑙𝑜𝑔(|𝑁(𝑢)|)]
- Katz centrality computes the centrality for a node based on the centrality of its neighbors. It is a generalization of the eigenvector centrality. 
- The Katz centrality for node i is 𝑥𝑖=𝛼∑𝑗[𝐴𝑖𝑗𝑥𝑗+𝛽], Controls the centrality with 𝛼<[1/𝜆𝑚𝑎𝑥].
- Weight Features 𝑊=1/SQRT[1+|𝑋|]

- FROM THE MODEL I FOUND THE BELOW FEATURES ARE INFLUCING THE MOST FOR THE FRIEND RECOMMENDATION
- - FOLLOW_BACKS
- WEIGHT_F1
- COSINE_FOLLOWERS
- SHORTEST_PATH
- INTER_FOLLOWERS
- WEIGHT_F3
- WEIGHT_F4
