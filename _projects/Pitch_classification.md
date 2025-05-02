---
name: Pitch Classification of Shohei Ohtani
tools: [Python, seaborn, Machine Learning, RandomForest, KNN, DecisionTree]
image: assets/pngs/Shohei_Ohtani.png
description: This will be a pitch classification model of Shohei Ohtani. (2023)

custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Introduction 

The purpose of this is to create a classification model to classify the type of pitch thrown by Shohei Ohtani based off ball statistics like velocity and rotation. The data revolves around historical pitching data taken from Statcast. The data will include speed of ball, spin rate, horizontal movement of the pitch, vertical movement of the pitch, side of the plate batter, and type of pitch.

Hopefully, the model can keep up with the GOAT. 

## Data

This is the data after being cleaned. 

<img title="Ohtani Data" alt="model data" src="/assets/pngs/ohtani_data.png">

## Visualization

The different pitch types are visualized in this graph. The graph makes it helpful in identifying pitch types depnding on the two features and seeing how they relate to the target variable.

<img title="Ohtani Data 2" alt="model graph" src="/assets/pngs/ohtani_data2.png">

## Models

3 different classification model is used to determine the most accurate classifer - KNN, random forest, and decision tree. To optimize the model performance, hyperparameters like the number of neighbors of the KNN is fine-tuned to find the number with the highest accuracy. Most parameters are kept the same between the different classification models to maintain a fair comparison and obtain the highest accuracy.

## Results

The KNN model is able to get high accuracy on both testing with 98.0% and training with 93.9%. This high accuracy shows that the model is able to classify pitch types accurately on both testing and training datasets. The report also confirms this by having a high weighted average for both test and train data. Although all the models have good accuracy, KNN has the highest accuracy especially in terms of testing accuracy. Decision tree and Random Forest show a high training accuracy of 100%; however they have lower testing accuracy. This is a clear case of overfitting where it does not generalize well to unseen test data.

## Conclusion

In conclusion, the KNN model is the best case for classifying different pitch types. It does not overfit and generalize well to the unseen data compared to decision tree and random forest classification models. Having the highest accuracy of 93.9% in testing accuracy, indicating a good balance of fitting training and testing data. Although the model has a high accuracy, I would not consider employing the model. There are too many factors in consideration that is left out from the dataset. There are numerous pitchers in the MLB with their own throwing style that will vasely differ from each other. The dataset only consider one pitcher and data from him will not apply to everyone. The model may have a high accuracy, but it can only confidently identify pitches thrown from Shohei Ohtani and not other pitchers. Pitchers can also learn new pitches or adapt new ones on the fly. The dataset will need to be updated constantly with new data and include data from other pitchers to make it viable in the MLB.