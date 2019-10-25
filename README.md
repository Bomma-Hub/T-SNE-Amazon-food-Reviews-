# T-SNE-Amazon-food-Reviews-
Implemntation of T-SNE on Amazon Food Reviews

Dimensionality Reduction:
Dataset with lot of features difficult to understand or explore the relationships between the features. Not only it makes the EDA process difficult but also affects the machine learning model’s performance since the chances are that you might over fit your model or violate some of the assumptions of the algorithm.
Dimensionality reduction can be achieved in the following ways:
•	Feature Elimination: You reduce the feature space by eliminating features. This has a disadvantage though, as you gain no information from those features that you have dropped.
•	Feature Selection: You apply some statistical tests in order to rank them according to their importance and then select a subset of features for your work. This again suffers from information loss and is less stable as different test gives different importance score to features. You can check more on this here.
•	Feature Extraction: You create new independent features, where each new independent feature is a combination of each of the old independent features. These techniques can further be divided into linear and non-linear dimensionality reduction techniques.

TSNE 
•	Reference: Journel on Visualizing Data using t-SNE by "Laurens van der Maaten" and "Geoffrey Hinton".
o	https://www.datacamp.com/community/tutorials/introduction-t-sne
o	https://www.youtube.com/watch?v=NEaUSP4YerM
•	The technique is a variation of Stochastic Neighbor Embedding (Hinton and Roweis, 2002).It is significantly better visualization by reducing the tendency to crowd points together in the center of the map.
•	Other non-parametric (non linear ) dimensionality/visualization techniques.
1.	Sammon mapping (Sammon, 1969).
2.	Isomap p (Tenenbaum et al., 2000)
3.	Locally Linear Embedding  (LLE; Roweis and Saul, 2000).
4.	Curvilinear components analysis (CCA; Demartines and Herault, ´ 1997).
5.	Stochastic Neighbor Embedding (SNE; Hinton and Roweis, 2002)
6.	Laplacian Eigenmaps (Belkin and Niyogi, 2002)
•	Techniques include iconographic displays such as 
1.	Chernoff faces (Chernoff, 1973),
2.	Pixel-based techniques (Keim, 2000), and techniques that represent the dimensions in the data as vertices in a graph (Battista et al., 1994). Most of these techniques simply provide tools to display more than two data dimensions, and leave the interpretation of the data to the human observer.
•	Keywords: visualization, dimensionality reduction, manifold learning, embedding algorithms, multidimensional scaling.

AIM:
•	The aim of dimensionality reduction is to preserve as much of the significant structure of the high-dimensional data as possible in the low-dimensional map.
•	The Aim is to match the similarity matrix of high dimensional space and similarity matrix of low dimensional space.
•	T-SNE is capable of capturing much of the local structure of the high-dimensional data very well, while also revealing global structure such as the presence of clusters at several scales

                                    
 
•	Principal Components Analysis (PCA; Hotelling, 1933) , classical multidimensional scaling (MDS; Torgerson, 1952) are linear techniques that focus on keeping the low-dimensional representations of dissimilar datapoints far apart.
SNE (Stochastic Neighbor Embedding):
Starts by converting the high-dimensional Euclidean distances between datapoints into conditional probabilities that represent similarities.
Euclidian Distance: Shortest distance between two objects or points in space. Alos known as L2-Norm of vector in vector space.
The square of the total distance between two objects is the sum of the squares of the distances along each perpendicular co-ordinate.


Euclidian Distance : D =  sqrt ( ( x2 - x1 ) ^ 2  +  ( y2 - y1 ) ^2)
 
•	The similarity of datapoint x j to datapoint xi is the conditional probability, p j|i , that xi would pick x j as its neighbor. 
•	For nearby datapoints, pj|i is relatively high, whereas for widely separated datapoints, p j|i will be almost infinitesimal.
•	Similarly for low dimensional points of high dimensional datapoints we calculate the conditional probability q j/i.
 
•	If the map points yi and y j correctly model the similarity between the high-dimensional datapoints xi and x j , the conditional probabilities p j|i and qj|i will be equal.
•	For every data point we need to get the neighbor’s. It is done based on its and variance and perplexity. Every datapoint has different variance as dense parts of region in high dimensional requires small variance and sparse parts of the region in highdimensioanl requires large variance to select neighbor’s.


T-SNE:
High Dimensional Data  -->  transform (use a distance metric) -- > Linear/Non-Linear Models -->manifold
---> Low Dimensional Data. 

 •	T-SNE embeds local structure more better i.e it keeps points that are close to very much close in lower dimensional fields by which moderately close or far points will more far in final map(in lower dimension).
•	The Algorithm places all the points on a 2D space Initially and then Interacts with each other based on two laws. 1) Repel 2)  Attract
 

 
To calculate similarity between high dimensional datapoints and low dimensional datapoints T-SNE uses Kullback-leibler divergence which is a cost function for T-SNE.
 

 
