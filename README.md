# **Currently a work in progress**


# YellowTaxiTips
This project aims to determine whether or not a yellow taxi driver would get a good tip.
The data contains information such as the trip's duration, distance, pickup and dropoff locations, etc. The data used can be found in the April 2019 dataset from https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page

- [Project Goal](#ProjGoal)
- [Number of Good Tips](#NumberGood)
- [The Model](#BestModel)
- [Distribution of Residuals](#DistRes)
- [Big Takeaways](#Takeaway)
<br>

## Project Goal <a name = 'ProjGoal'></a>
The purpose of this project is to predict whether a yellow taxi driver would get a good tip or not. A good tip is determined as at least 25% of the base fare amount.
<br>
<br>

## How Many Tips Are Good Tips? <a name = 'NumberGood'></a>

<center><img src='graphs/dist_of_good_bad_tips.png' width = 550></center>
One important piece of information is the number of tips that are considered "good" in the data. The bar graph above shows us that there are fewer tips that are good than not. Although there isn't much class imbalance, upsampling was used so that the models would not be biased to choose the majority class (not good tip) more often than it should.
<br>
<br>

## The Best Performing Model <a name = 'BestModel'></a>
The models that were run were logistic regressions with L1 and then L2 regularization, and a random forest model. Out of these models, the model that performed the best was the random forest model with a test accuracy of 0.953 and an f1 score of 0.945. This meant that the model was able to predict whether or not the trip would have a good tip fairly well.
<br>
<br>
The random forest model can also tell us which features would give us the most information. This is done by determining which features were used the most in the decision trees when splitting the data. A graph displaying feature importance can be seen below:
<br>
<img src = "graphs/feature%20importance%20chart.PNG" width = 550>
<br>
We see that features such as the trip's total cost, duration, and distance are important features. However, what this doesn't tell us how these features are important. Does a longer or shorter trip usually result in a good tip? Do yellow taxi drivers usually get a good tip when the total cost of the ride is higher or lower? In order to answer this, we need to look back at the data.

## Distribution Of Features To Amount Of Good Tips
The feature that provides the most information is the trip's total cost. Below shows a scatterplot of the total price categorized by whether the tip was good or not:
<br>
<img src = "graphs/tip_well_vs_total.png" width = 550>
We can see that there is a cut off of almost $4 until yellow taxi drivers even get a good tip. 
