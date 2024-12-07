# vignette-Recommender-MF

Vignette on application of advanced recommender system algorithm, Matrix Factorization, using Amazon electronic product review data; created as a class project for PSTAT197A in Fall 2024.

# Contributors

Brian Lu, Candis Wu, Caitlyn Vasquez, Colin Nguyen, Carter Kulm


# Vignette Abstract

In this vignette, we explore a more advanced method of building a recommender system with the help of deep learning algorithms. When working with a large and sparse user-item matrix in collaborative filtering tasks, we usually want to decompose the large and sparse matrix into smaller matrices for efficiency and accuracy. As opposed to the typical SVD decomposition of the user-item matrix into a latent user matrix and a latent item matrix, which are more compact, we discovered another approach with more freedom implementing deep learning. Say the large user-item matrix has dimension $n \times m$, we want to define a $n \times k$ user matrix and a $k \times m$ user matrix, with k being a hyper-parameter. The product of these two matrices will be out prediction of every user's rating on every items. The error in this case would be the difference between the estimated rating and the true rating we have, calculated by RMSE. We then train the parameters (values in the user and item matrix) to minimize the $l2$ error with weight decay to reach the optimized latent matrices to generate predictions.


# Repository Contents

The data we will be working with is a set of Amazon electronic product reviews that includes a user ID, product ID, rating, and time stamp for each purchase. For our purposes we will not be using the time stamps. 
The `vignette.qmd` file will serve as our group's primary vignette document and will include specific code chunks and their explanations that teach the reader about the matrix factorization method being shown. Selected results will be shown at the end of the document that illustrate the predictions given by the model. 

The script included in our repository will contain all code used to build the model along with line-by-line annotations that make it easier to understand or replicate the methods put to use. The chunks included in the primary vignette document will be drawn from this script.


# Reference List

 - Reference 1: Zhang, A., Lipton, Z. C., Li, M., & Smola, A. J. (2021). Matrix factorization for recommender systems. *Dive into Deep Learning*. Retrieved from https://www.d2l.ai/chapter_recommender-systems/mf.html

 - Reference 2: Pazzani, M. J., & Billsus, D. (1997). Learning and revising user profiles: The identification of interesting web sites. *Machine Learning, 27*(3), 313–331. Retrieved from https://ics.uci.edu/~pazzani/Publications/MLC98.pdf
 
 - Reference 3: Hodges, J. S., & Sargent, D. J. (2009). Counting degrees of freedom in hierarchical and other richly parameterized models. *Biometrika, 96*(1), 73–84. Retrieved from https://www.asc.ohio-state.edu/statistics/statgen/joul_aut2009/BigChaos.pdf
 
 - Reference 4: Gomez-Uribe, C. A., & Hunt, N. (2015, April 6). Netflix recommendations: Beyond the 5 stars (Part 1). *Netflix Tech Blog*. Retrieved from https://netflixtechblog.com/netflix-recommendations-beyond-the-5-stars-part-1-55838468f429