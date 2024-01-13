# House Price Prediction
this project uses the dataset of california house prices in a block with the following fields
1. longitude: A measure of how far west a house is; a higher value is farther west
2. latitude: A measure of how far north a house is; a higher value is farther north
3. housingMedianAge: Median age of a house within a block; a lower number is a newer building
4. totalRooms: Total number of rooms within a block
5. totalBedrooms: Total number of bedrooms within a block
6. population: Total number of people residing within a block
7. households: Total number of households, a group of people residing within a home unit, for a block
8. medianIncome: Median income for households within a block of houses (measured in tens of thousands of US Dollars)
9. medianHouseValue: Median house value for households within a block (measured in US Dollars)
10. oceanProximity: Location of the house w.r.t ocean/sea

## Problems 
the main problem faced were the following:-
1. the field ocean proximity was not an integer format 
2. there are nan values present in the total_bedrooms field
3. there was a need to scale the feature and intoduce new features like bedroom_ratio and household_ratio
4. the data for some fields were skewed 

## preprocessing of the data 
1. one hot encoding of the ocean proximity field
2. drop the nan values ( as they are not a lot of nan values )
3. feature engineering of the features which turned out to have a better correlation
4. using numpy to fix the skewed data

## Approach Taken
we use the random forest regressor model 
### random forest regressor 
- Random Forest Regressor is an ensemble learning method that can be used to predict continuous targets.
- It works by creating individual decision trees at each split and merging them together to get the finaldecision. This process helps to reduce overfitting and improve generalization on unseen data.
### cross validation
we use grid search cross validation to get the accuracy a little better and the final accuracy is at 81.8%
