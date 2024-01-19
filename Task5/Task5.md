# Task 5
## Exercise 1
### Output
Large drift, new accuracy:  0.69
Small drift, new accuracy:  0.865

In our example, we first create a dataset with normal data on which we train our model. 
Afterward, we test our model on an equal data, but we add values based on a random factor * drift_factor. 
This would mean that we have a feature drift in our data, and our data is shifted.

## Exercise 2
Predicting if a car is fast or slow from car features.

### Concept Drift
An speed level of cars that was earlier considered fast is now a lot slower.

### Label Drift
A larger portion of fast cars start showing up. 

### Feature Drift
Prices of most cars increase or decrease. Or we are getting suddenly a lot more cars from one region.

### Seasonal Drift
​Example: Bear attacks on people.
Bears hibernate over the winter and as a result, bear attacks probably decrease during this period.