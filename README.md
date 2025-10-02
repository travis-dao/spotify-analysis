# Spotify Analysis
Build machine learning model to predict user churn, analyze engagement patterns, and help Spotify reduce cancellations.

## Dataset
- [Source](https://www.kaggle.com/datasets/nabihazahid/spotify-dataset-for-churn-analysis/data)
- Type: Mixed (numeric + categorical)
- Rows: Each row represents a unique Spotify user.
- Columns (Features):

### Features
| Feature | Description |
| ------ | ------ |
| user_id | Unique identifier for each user (remove during data processing) |
| gender | User gender (Male/Female/Other) |
| age | User age |
| country | User location |
| subscription_type | Type of Spotify subscription (Free, Premium, Family, Student) |
| listening_time | Minutes spent listening per day |
| songs_played_per_day | Number of songs played daily |
| skip_rate | Percentage of songs skipped |
| device_type | Device used (Mobile, Desktop, Web) |
| ads_listened_per_week | Number of ads heard per week |
| offline_listening | Offline mode usage |

### Target
- is_churned → 0 = Active, 1 = Churned


## Model
RandomForestClassifier (sklearn)

### Accuracy
Random forest accuracy: 0.7381

### Thoughts
In this project, we are only predicting whether a spotify user will churn. Due to this nature, a lower accuracy score is acceptable, whereas in a higher risk setting, medical field, this is unacceptable.

Generally, what constitutes a "good" model accuracy is somewhat abitrary, with the commonly agreed upon range between 70% to 90% for real world use cases. However, we have to keep in mind that there exists many external factors that can inhibit our ability to increase our model accuracy. The common issues include: non-linear data, number of data, quality of data, model complexity, and model efficieny. 

An issue with this model is the lack of data, with there being only 8000 samples. Taking into consideration that there are around 700 million current spotify users, this discrepency in sample size could be a problem to building a better model. Therefore, considering the sample of size of 8000, the model accuracy of around 74% is acceptable.

## Analysis
### Feature Importance

![alt text]([https://github.com/[username]/[reponame]/blob/[branch]/image.jpg](https://github.com/travis-dao/spotify-analysis/blob/main/feature%20importances.jpeg))
