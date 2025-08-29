Employee Attrition Prediction using Deep Learning
This project develops a deep learning model to predict employee attrition. By analyzing various employee-related features, the model aims to identify factors contributing to attrition and provide an early warning system for organizations.

Project Structure
The core of this project is a Jupyter Notebook that performs the following steps:

Data Loading and Initial Exploration:

The employee_attrition.csv dataset is loaded using pandas.

Basic data information is checked using df.info() and df.head().

Exploratory Data Analysis (EDA):

The distribution of the target variable, Attrition, is visualized using a pie chart to check for class imbalance.

Key relationships between features and attrition are explored through visualizations, including:

A count plot of Attrition by JobLevel.

A box plot of AvgWorkHoursPerWeek by Attrition.

A bar chart of Attrition Rate by Country.

A correlation heatmap of all numerical features.

A histogram of LastEvaluationScore by Attrition.

Data Preprocessing:

Missing values in the Age, MonthlyIncome, and LastEvaluationScore columns are filled with the median to ensure data integrity.

Categorical features (Gender, Country, Department, JobLevel) are converted to numerical values using LabelEncoder.

The EmployeeID column is dropped as it is not needed for the model.

The data is split into training and testing sets.

The imbalanced training data is resampled using SMOTE (Synthetic Minority Over-sampling Technique) to create a more balanced dataset for training.

All features are scaled using StandardScaler to normalize the data.

Model Building and Training:

A deep learning model is built using TensorFlow's Keras Sequential API.

The model consists of three dense layers with relu and sigmoid activation functions.

It is compiled with the adam optimizer and binary_crossentropy loss function.

The model is trained on the resampled and scaled training data for 30 epochs.

Model Evaluation:

The trained model's performance is evaluated on the unseen test data.

The final accuracy score is printed.

A confusion matrix is generated to visualize the model's predictions.

A plot of training and validation accuracy over the epochs is shown to monitor the model's learning process.
