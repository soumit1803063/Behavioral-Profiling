## Project Overview

This project aims to predict and analyze behavioral traits using weekly activity patterns and demographic information. The dataset combines **weekday and weekend activity data** with **demographic characteristics** to explore relationships between daily routines and personality traits. The project involves data preprocessing, exploratory data analysis, feature engineering, and predictive modeling to deliver insights into lifestyle patterns and behaviors.

## Dataset Columns

### Activity Metrics (Continuous)

These columns represent time spent on specific activities on weekdays and weekends, measured in hours:

- **C_wk**: Computer usage time during weekdays, capturing the hours spent on computers, potentially indicating work or leisure activities.
- **C_wn**: Computer usage time during weekends, reflecting leisure or additional work hours on computers outside of the workweek.
- **G_wk**: Game time during weekdays, representing hours dedicated to gaming, which may serve as a stress reliever or recreational activity.
- **G_wn**: Game time during weekends, often reflecting increased leisure time for gaming activities.
- **S_wk**: Sedentary activity during weekdays, typically hours spent sitting for work or studying, indicating physical inactivity.
- **S_wn**: Sedentary activity during weekends, reflecting downtime or leisure periods involving sitting activities such as watching TV or reading.
- **T_wk**: Television/Tablet time during weekdays, capturing entertainment or relaxation time after daily routines.
- **T_wn**: Television/Tablet time during weekends, highlighting leisure time usage of visual media.


### Demographic Attributes (Categorical)

Demographic features may influence or relate to activity and behavioral trends:

- **Gender**: 0 for male, 1 for female.
- **Minority**: Minority status (1 for minority, 0 otherwise).
- **Deprived**: Socioeconomic deprivation status (1 for deprived, 0 otherwise).

### Target Variables (Categorical, Ordinal Scale)

These variables, scored from 1 to 5, represent different behavioral or emotional traits. They provide insight into individuals' mindsets and emotional characteristics, which can correlate with their activity levels and demographics:

- **Optm**: Optimism level, where higher values reflect greater optimism.
- **Usef**: Perceived usefulness or purposefulness, with higher values indicating a stronger sense of purpose.
- **Relx**: Relaxation level, with higher scores indicating better relaxation abilities.
- **Intp**: Interpretive ease, showing how easily individuals interpret situations, with higher values reflecting greater ease.
- **Engs**: Engagement level, with higher scores suggesting a more active involvement in tasks or hobbies.
- **Dealpr**: Ability to deal with pressure, where higher values indicate better pressure handling.
- **Thcklr**: Thick-skinned nature, with higher values representing greater resilience.
- **Goodme**: Good memory, with higher scores indicating better memory capabilities.
- **Clsep**: Closeness to others emotionally, with higher values reflecting stronger emotional connections.
- **Conf**: Confidence level, where higher values show greater self-assurance.
- **Mkmind**: Ability to make up one's mind, with higher scores indicating quicker decision-making.
- **Loved**: Feeling of being loved, with higher values showing a stronger sense of being appreciated.
- **Intthg**: Interest in thoughtful behavior, with higher scores suggesting a more reflective nature.
- **Cheer**: Cheerfulness, where higher values reflect a generally positive demeanor.

These traits offer insights into individuals' personalities and mindsets, potentially linked to their activity patterns.

## Project Workflow

1. **Data Splitting**:
   - The dataset is split into **training** and **testing sets** using an 80-20 split. The feature set `X_pca` and target variables `y` are split with `train_test_split`.

2. **Model Training and Hyperparameter Tuning**:
   - Three regression models are applied: **Linear Regression**, **Ridge Regression**, and **Lasso Regression**.
   - **Linear Regression** is trained directly without hyperparameter tuning.
   - **Ridge Regression** and **Lasso Regression** models undergo hyperparameter tuning using `GridSearchCV`, with `alpha` values ([0.01, 0.1, 1, 10, 100]) and **cross-validation** (5-fold) to optimize for `neg_mean_squared_error`.

3. **Prediction**:
   - Each model predicts the target variables on the test set. Predictions are generated separately for Linear, Ridge, and Lasso models.

4. **Evaluation Metrics**:
   - Models are evaluated using three metrics:
     - **Mean Squared Error (MSE)**: Measures the average squared differences between predicted and actual values.
     - **Mean Absolute Error (MAE)**: Measures the average magnitude of errors in predictions.
     - **R2 Score (R2)**: Indicates the proportion of variance in the target variables explained by the model.

   Results are printed for each model, offering comparative insights into performance.

5. **Visualization**:
   - Scatter plots visualize predictions against actual values for each model (Linear, Ridge, Lasso) and each target variable, helping assess model accuracy visually.

This workflow provides insights into how activity and demographic features predict behavioral traits, exploring model effectiveness and feature influence.
