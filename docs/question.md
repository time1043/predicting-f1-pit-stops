## Overview

**Welcome to the 2026 Kaggle Playground Series!** We plan to continue in the spirit of previous playgrounds, providing interesting and approachable datasets for our community to practice their machine learning skills, and anticipate a competition each month.

**Your Goal:** Predict whether a Formula 1 driver will pit on the next lap.

### Evaluation

Submissions are evaluated on [area under the ROC curve](http://en.wikipedia.org/wiki/Receiver_operating_characteristic) between the predicted probability and the observed target.

## Submission File

For each id in the test set, you must predict a probability for the `PitNextLap` target. The file should contain a header and have the following format:

```
id,PitNextLap
439140,0.2
439141,0.3
439142,0.9
etc.
```

### Timeline

- **Start Date** - May 1, 2026
- **Entry Deadline** - Same as the Final Submission Deadline
- **Team Merger Deadline** - Same as the Final Submission Deadline
- **Final Submission Deadline** - May 31, 2026

All deadlines are at 11:59 PM UTC on the corresponding day unless otherwise noted. The competition organizers reserve the right to update the contest timeline if they deem it necessary.

### About the Tabular Playground Series

The goal of the Tabular Playground Series is to provide the Kaggle community with a variety of fairly light-weight challenges that can be used to learn and sharpen skills in different aspects of machine learning and data science. The duration of each competition will generally only last a few weeks, and may have longer or shorter durations depending on the challenge. The challenges will generally use fairly light-weight datasets that are synthetically generated from real-world data, and will provide an opportunity to quickly iterate through various model and feature engineering ideas, create visualizations, etc.

### Synthetically-Generated Datasets

Using synthetic data for Playground competitions allows us to strike a balance between having real-world data (with named features) and ensuring test labels are not publicly available. This allows us to host competitions with more interesting datasets than in the past. While there are still challenges with synthetic data generation, the state-of-the-art is much better now than when we started the Tabular Playground Series two years ago, and that goal is to produce datasets that have far fewer artifacts. Please feel free to give us feedback on the datasets for the different competitions so that we can continue to improve!

### Prizes

**Please note:** In order to encourage more participation from beginners, Kaggle merchandise will only be awarded once per person in this series. If a person has previously won, we'll skip to the next team.

### Citation

Yao Yan, Walter Reade, Elizabeth Park. Predicting F1 Pit Stops. https://kaggle.com/competitions/playground-series-s6e5, 2026. Kaggle.

## Dataset Description

The dataset for this competition (both train and test) was inspired by [F1 strategy dataset](https://www.kaggle.com/datasets/aadigupta1601/f1-strategy-dataset-pit-stop-prediction/data). Feature distributions are close to, but not exactly the same, as the original, and we intentionally remove `Normalized_TyreLife` which makes the prediction trivial. Feel free to use the original dataset as part of this competition, both to explore differences as well as to see whether incorporating the original in training improves model performance.

### Files

- **train.csv** - the training set, with `PitNextLap` as target
- **test.csv** - the test set, used to predict the likelihood for `PitNextLap`
- **sample_submission.csv** - a sample submission file in the correct format

### Summary

- 77.72 MB
- 3 files
- 33 columns

### License

[Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/)
