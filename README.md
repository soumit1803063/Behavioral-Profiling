## Dataset Column Descriptions

The dataset is composed of **weekly activity metrics** split between **weekday (wk)** and **weekend (wn)** usage patterns, alongside **demographic information**. Here is a detailed breakdown of each column:

### Activity Features (Continuous)

These columns represent time spent on specific activities on weekdays and weekends, measured in hours:

- **C_wk**: Computer usage time during weekdays, capturing the hours spent on computers, potentially indicating work or leisure activities.
- **C_wn**: Computer usage time during weekends, reflecting leisure or additional work hours on computers outside of the workweek.
- **G_wk**: Game time during weekdays, representing hours dedicated to gaming, which may serve as a stress reliever or recreational activity.
- **G_wn**: Game time during weekends, often reflecting increased leisure time for gaming activities.
- **S_wk**: Sedentary activity during weekdays, typically hours spent sitting for work or studying, indicating physical inactivity.
- **S_wn**: Sedentary activity during weekends, reflecting downtime or leisure periods involving sitting activities such as watching TV or reading.
- **T_wk**: Television/Tablet time during weekdays, capturing entertainment or relaxation time after daily routines.
- **T_wn**: Television/Tablet time during weekends, highlighting leisure time usage of visual media.

### Demographic Features (Categorical)

These categorical columns represent demographic attributes, which may influence activity patterns and target behaviors:

- **Gender**: Binary category, where 0 represents male and 1 represents female, used to examine activity and behavior trends across genders.
- **Minority**: Binary category indicating minority status (1 for minority, 0 otherwise), which could help reveal patterns specific to minority groups.
- **Deprived**: Binary category indicating if a person is from a deprived socioeconomic background (1 for deprived, 0 otherwise), which might impact activity levels and access to resources.

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

## Project Work Overview

This project focuses on **analyzing** and **predicting** behavioral traits based on activity patterns and demographic data. The tasks involved include:

1. **Data Preprocessing**: Cleaning the dataset, handling any missing values, encoding categorical variables, and normalizing or scaling continuous features for consistency across models.

2. **Exploratory Data Analysis (EDA)**: Conducting statistical analysis and visualization to uncover correlations and patterns between activity metrics, demographics, and behavioral traits.

3. **Feature Engineering**: Creating new features, if necessary, to improve model performance, such as aggregating weekday and weekend activity levels or generating interaction terms between demographics and activities.

4. **Model Training and Evaluation**:
   - **Classification Models**: Developing and tuning several classification algorithms, such as logistic regression, SVM, decision trees, and random forests, to predict each behavioral trait.
   - **Evaluation Metrics**: Using metrics such as accuracy, precision, recall, and F1-score to evaluate model performance, with special attention to the interpretability of each model in understanding behavioral trends.

5. **Insights and Reporting**: Documenting the findings, including key correlations, model performance insights, and any notable patterns observed in the relationship between activity, demographics, and behavioral traits. The final report aims to provide actionable insights into lifestyle patterns and personality traits based on the dataset.

By combining activity and demographic data, this project sheds light on how daily routines and background factors contribute to individual behavioral characteristics, potentially helping guide targeted interventions or recommendations for lifestyle improvements.
