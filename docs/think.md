## Submit

- `sample_submission.csv`
- PitNextLap is a **probability** (0-1), not hard label

## Evaluation

- AUC-ROC (area under ROC curve)
- Measures ranking quality of predicted probabilities vs true labels

## Explore Data

### Train & Test

- Train: (439140, 16)
- Test: (188165, 15)
- Input: 15 features
- Target: 1 column `PitNextLap`

### PitNextLap

- In Train: binary (0 or 1), 19.9% positive (87,381 / 439,140)
- In Test: submit probability (0-1), actual labels unknown

### Columns

- Categorical: `Driver`, `Compound`, `Race`
- Numeric: `Year`, `PitStop`, `LapNumber`, `Stint`, `TyreLife`, `Position`, `LapTime (s)`, `LapTime_Delta`, `Cumulative_Degradation`, `RaceProgress`, `Position_Change`
- ID: `id`
- Target: `PitNextLap`
- No missing values

- Some features already engineered (`LapTime_Delta`, `Cumulative_Degradation`, `RaceProgress`)
- Dataset description mentions 33 columns but actual data has 16

## Model

- Start with XGBoost, LightGBM baseline
- Validate with time-based split (not random)
