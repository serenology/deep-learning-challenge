# deep-learning-challenge

For submission for bootcamp challenge.

## Credit

All code was written by Seren Frazin with assistance from ChatGPT.

## Analysis

The purpose of this learning model was to determine with accuracy that can predict whether applicants will be successful if funded by Alphabet Soup.

### Data Preprocessing
- Target Variable: The target for the model is IS_SUCCESSFUL, indicating whether the charity application was successful.
- Feature Variables: Features include various characteristics of the applications, such as application type, affiliation, classification, use case, organization, status, income amount, special considerations, and ask amount, after preprocessing steps like encoding categorical variables and dropping non-informative columns.
- Variables Removed: EIN and NAME were removed from the input data as they are identifiers that do not contribute to the model's ability to predict the outcome.

### Compiling, Training, and Evaluating the Model
- Model Architecture: The model architecture evolved through iterations. Initially, it started with a simpler structure, and layers were added, and activation functions were changed (e.g., ReLU to Leaky ReLU) to improve performance. The final iteration discussed included layers with different numbers of neurons (e.g., 128, 64, 32) and used Leaky ReLU as an activation function to help mitigate the vanishing gradient problem. Dropout layers were also introduced to prevent overfitting.
- Achieving Target Performance: The target model performance aimed to surpass 75% accuracy. Through iterations, improvements were made, but achieving or exceeding the target performance required continuous adjustments in model architecture, data preprocessing, and training configurations.
- Steps to Increase Performance: Efforts to increase model performance included:
    - Adjusting the model architecture by adding more layers and neurons.
    - Changing activation functions to improve learning dynamics.
    - Experimenting with data preprocessing, such as creating more bins for categorical variables to reduce the impact of rare occurrences.
    - Tuning hyperparameters like epochs and batch size.

### Summary and Recommendations
The overall results of the deep learning model showed incremental improvements in accuracy with each iteration, reflecting the complexity and challenges of predicting successful charity applications based on the provided features. Despite these efforts, consistently exceeding the 75% accuracy benchmark proved challenging, suggesting that further experimentation with model architecture, data preprocessing, and perhaps different types of neural network models could be beneficial.

**Recommendation for a Different Model:** Considering the challenge at hand, exploring other models like Random Forest or Gradient Boosting could be advantageous. These models can capture non-linear relationships in the data and might offer better performance with less need for manual feature engineering and hyperparameter tuning than deep neural networks. They also provide feature importance metrics, which can be valuable for understanding which variables most strongly predict the target outcome.

**Explanation:** Ensemble methods like Random Forest and Gradient Boosting are robust to overfitting and can handle categorical and numerical data well. They might achieve high performance with less preprocessing and tuning effort. Given their proven track record in classification tasks, it's worth conducting a comparative analysis to see if these models offer an improvement over the deep learning approach for this specific problem.

In summary, while deep learning models offer powerful capabilities, their performance heavily depends on the architecture, data quality, and the tuning of hyperparameters. Alternative models like ensemble methods could provide a simpler or more effective solution for certain classification problems.