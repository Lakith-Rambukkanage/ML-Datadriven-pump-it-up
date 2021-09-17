# ML-Datadriven-pump-it-up

## Repo
[link to github repo](https://github.com/Lakith-Rambukkanage/ML-Datadriven-pump-it-up)

## EDA
Dataframe built in methods hist(), value_counts(), unique(), info(), describe() were used
Also Seaborn was used to plot relations to the predictor.
## Preprocessing
Missing values and Errored values were filled with means and defaults
Boleans were converted to numerics.
Strings were transformed to numerics when possible. ex-date
## Feature engineering

### Mathematical tranformations
Year difference

Year difference squared

Polar transforms 

    lon_lat_tan = Longitude / Latitude (tan)

    lon_lat_r = (Longitude **2 + Latitude **2) **0.5

gps_height_sqr = gps_height**2 

### Ordinal encoding & Intuitive Lable Mapping
Ordinal encoding was used when possible
Ordinal values were intuitively added for some lables and tested : values were assigned based on the robusness impact on pumps basd on the values

### One hot encoding (Dummy) encoding 
One hot encoding were using for lables with less unique values and accuracy was observed

### Target encoding 
Functional : 1 need repair: 0 non-functional:-1 was used to make the predictor numeric for target encoding
This predictor was used as the target variable to encode lables with more number of unique values

## Feature importance
1. Weight: The number of times a feature is used to split the data across all trees.

![Feature importance based on weight](https://github.com/Lakith-Rambukkanage/ML-Datadriven-pump-it-up/blob/main/XG%20boost%20importance%20snaps/xg%20boost%20importance%20weight.png)

2. Cover: The number of times a feature is used to split the data across all trees weighted by the number of training data points that go through those splits.

![Feature importance based on cover](https://github.com/Lakith-Rambukkanage/ML-Datadriven-pump-it-up/blob/main/XG%20boost%20importance%20snaps/xg%20boost%20importance%20cover.png)

3. Gain: The average training loss reduction gained when using a feature for splitting.

![Feature importance based on gain](https://github.com/Lakith-Rambukkanage/ML-Datadriven-pump-it-up/blob/main/XG%20boost%20importance%20snaps/xg%20boost%20importance%20gain.png)


Pump it up rank at data driven
![Rank](https://github.com/Lakith-Rambukkanage/ML-Datadriven-pump-it-up/blob/main/Pump%20it%20Up%20snap.png)