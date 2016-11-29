---
layout: post
title: IMDb Ratings
---

## IMDb Ratings

#### Problem Statement:

The goal is to determine which features contribute most to a higher rating on IMDb. To determine this we'll gather various data about a movie from IMDb using any of various API's. We'll then build a number of regression models to determine which model optimizes the loss function (MSE). In order to determine which features are most important we'll use Recursive Feature Elimination for each model, as well as, calling the feature importance method on the winning model. This should provide an accurate representation of which features are most important for determine the rating of a movie.

#### Data Risk and Assumptions:

We're pulling the top 250 movies, which naturally will have some selection bias associated with it. We're going to ignore that for now.
Some values were missing and had to be imputed.
IMDb as a source is about as reliable as you can hope for, but there could be discrepancies in the data. e.g. the way you report 'Gross' has changed some over time.
There's a lot of collinearity in the data. We're using recursive feature selection with each of our models to help account for some of that.
Model Selection:

We've looked at a number of tree-based regression models to determine the which model will perform best given our data. We've decided on the following models


#### Model Performance:

Model
MSE
R2
Random Forest Regressor
0.021
0.46
Ada Boost Regressor
(base Decision Tree Regressor)
0.0271
0.30
Gradient Boosting Regressor¶
0.0226
0.42
Extra Trees Regressor
0.0189
0.51

#### Best Model:

For our scoring metric we primarily looked at the MSE to judge how well the model performed. The R2 was also included as a measure of how well the model was explaining the increasing in rating but was not the primary measure.
The Extra Trees Model performed best in both measures with an MSE of 0.019 and an R2 of 0.51. This is an expected outcome because Extra Trees performs well in many senarios. The extra randomness produces a result where the errors are less correlated with eachother. (http://www.montefiore.ulg.ac.be/~ernst/uploads/news/id63/extremely-randomized-trees.pdf)


#### Most Significant Features:


importance
imdbVotes
0.514188
Year
0.133010
Runtime
0.092335
writer_ mario puzo
0.077557
Gross
0.073949
genre_drama
0.045207
writer_ mickey knox
0.037617
country_usa
0.026137

#### Conclusion:


Finally, above we call the feature importance method on our model to determine which features have the largest impact. Since this is a tree-based model we won't have coefficients but we do get the feature importance score, which, is (per the documentation) the "[...] (normalized) total reduction of the criterion brought by that feature. "
