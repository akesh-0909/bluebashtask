
# Beer Rating Prediction Project

This project aims to predict the overall rating of beers based on various review features, using machine learning models to evaluate predictive accuracy.

## Project Overview

The goal is to predict the **overall rating** (`review/overall` column) from a dataset of beer reviews. This involves using several features that describe the beer's characteristics and the user's review details.

## Features

The dataset includes the following features:

- **index**: Identifier for the review
- **beer/beerId**: Unique ID for the beer
- **beer/ABV**: Alcohol by volume percentage of the beer
- **beer/brewerId**: Unique ID for the brewery
- **beer/name**: Name of the beer
- **beer/style**: Style or type of beer
- **review/appearance**: Rating of appearance (1.0 to 5.0)
- **review/aroma**: Rating of aroma (1.0 to 5.0)
- **review/overall**: Overall rating (1.0 to 5.0) - `Target variable`
- **review/palate**: Rating of palate (1.0 to 5.0)
- **review/taste**: Rating of taste (1.0 to 5.0)
- **review/text**: Text content of the review
- **review/timeStruct**: Dictionary specifying submission time
- **review/timeUnix**: Unix timestamp of submission
- **user/ageInSeconds**: Age of the user in seconds
- **user/birthdayRaw**: User's birthday in raw format
- **user/birthdayUnix**: User's birthday as Unix timestamp
- **user/gender**: Gender of the user (if specified)
- **user/profileName**: Profile name of the user

## Evaluation Metrics

To evaluate the performance of the model, the following metrics were used:

- **Mean Absolute Error (MAE)**
- **R² Score**
- **F1 Score**
- **Accuracy**
- **Custom Precision Score**
- **Custom Recall Score**

## Experiments Log

All model experiment results, including training and testing metrics, are stored in:
```bash
logs/logs.txt
```

## Dependencies

The project requires the following libraries (install if necessary):
```bash
pip install wordcloud
pip install xgboost
```

Here’s a **Conclusion** section that wraps up the project in the `README.md`:

---

## Conclusion

The Beer Rating Prediction Project successfully demonstrates the potential of using text-based features such as review text, beer style, and beer name, in addition to numerical features, to predict beer ratings. Key findings include:

- **Review Text and Beer Style, Name Matter**: An experiment with a model trained only on review text, beer style, and beer name achieved relatively high accuracy and F1 scores, indicating that these text-based features alone hold significant predictive power. This suggests that users’ qualitative feedback and beer characteristics contribute greatly to the final rating.
  
- **Model Performance with All Features**: Using all features (review, beer characteristics, and user information) improves model performance slightly, yet the gain is modest. This implies that while additional features add value, the core predictive information resides in the beer's descriptive characteristics and user review text.

- **Model Selection**: Logistic Regression was selected as the final model due to its balanced performance and interpretability, particularly on the review-related features. This model showed strong performance in classification metrics and proved to be a reliable choice for this prediction task.

Overall, the project underscores the importance of text-based review analysis in predictive modeling for ratings. Future improvements could involve Decomposition to reduce dimentionality, exploring more advanced NLP techniques or using ensemble models to further refine the prediction accuracy.

