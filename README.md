# vignette-Recommender-MF

An overview and application of advanced recommender system algorithm, Matrix Factorization

# Contributors

Brian Lu, Candis Wu, Caitlyn Vasquez, Colin Nguyen, Carter Kulm

# Vignette Abstract

In this vignette, we explore a more advanced method of building a recommender system with the help of deep learning algorithms. When working with a large and sparse user-item matrix in collaborative filtering tasks, we usually want to decompose the large and sparse matrix into smaller matrices for efficiency and accuracy. As opposed to the typical SVD decomposition of the user-item matrix into a latent user matrix and a latent item matrix, which are more compact, we discovered another approach with more freedom implementing deep learning. Say the large user-item matrix has dimension $n \times m$, we want to define a $n \times k$ user matrix and a $k \times m$ user matrix, with k being a hyper-parameter. The product of these two matrices will be out prediction of every user's rating on every items. The error in this case would be the difference between the estimated rating and the true rating we have, calculated by RMSE. We then train the parameters (values in the user and item matrix) to minimize the $l2$ error with weight decay to reach the optimized latent matrices to generate predictions.

# Repository Contents

The dataset we will be working with is ... Our primary vignette document is ... The script included in our repository is ...

# Reference List

Reference 1: ... Reference 2: ...
