# **Currently a work in progress**


# YellowTaxiTips
This project aims to determine whether or not a yellow taxi driver would get a good tip.
The data contains information such as the trip's duration, distance, pickup and dropoff locations, etc. The data used can be found in the April 2019 dataset from https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page

<!--
- [Project Goal](#ProjGoal)
- [Number of Good Tips](#NumberGood)
- [Scatterplot With An Independent Variable](#EDA)
- [Distribution of Residuals](#DistRes)
- [Big Takeaways](#Takeaway)
<br>

## Project Goal <a name = 'ProjGoal'></a>
The purpose of this project is to predict whether a yellow taxi driver would get a good tip or not. A good tip is determined as at least 25% of the base fare amount.
<br>
<br>

## How Many Tips Are Good Tips? <a name = 'NumberGood'></a>

<center><img src='graphs/dist_of_good_bad_tips.png' width = 400></center>
One important piece of information is the number of tips that are considered "good" in the data. The bar graph above shows us that there are fewer tips that are good than not. Although there isn't much class imbalance, upsampling was used so that the models would not be biased to choose the majority class (not good tip) more often than it should.
