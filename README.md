🌳 Procurement Viability Prediction

A machine learning classification project focused on predicting the viability of procurement opportunities based on historical procurement and contextual data.

The project covers the complete machine learning workflow, from exploratory data analysis and preprocessing to model comparison, hyperparameter optimization and deployment of the final trained model.

🎯 Objective

The goal of the project is to develop a classification model capable of determining whether a procurement opportunity is viable or non-viable based on characteristics such as procurement conditions, bidding information, economic indicators and geographic variables.

🔎 Project Workflow

The analysis follows an end-to-end machine learning pipeline:

* Exploratory Data Analysis (EDA)
* Data quality and missing-value analysis
* Feature selection and transformation
* Numerical feature scaling
* One-hot encoding of categorical variables
* Train/test dataset splitting
* Training and comparison of multiple classification algorithms
* Evaluation using accuracy, balanced accuracy and recall
* Hyperparameter optimization
* Cross-validation using K-Fold
* Selection and retraining of the best-performing model
* Model serialization using Joblib for future predictions

🤖 Models Evaluated

Several machine learning algorithms were trained and compared:

* K-Nearest Neighbors (KNN)
* Logistic Regression
* Decision Tree
* Random Forest

Each model was evaluated against the same prediction task to identify the approach providing the strongest classification performance.

🏆 Final Model — Random Forest

Random Forest provided the best overall predictive performance and was therefore selected as the final model.

The model was further optimized using GridSearchCV and K-Fold cross-validation, exploring parameters including:

* Maximum tree depth
* Minimum samples required to split a node
* Minimum samples per leaf
* Number of features considered at each split

The optimized model was subsequently retrained using the complete available dataset and exported as a .joblib file for reuse on unseen data.

⚙️ Data Preprocessing

A Scikit-learn pipeline was used to ensure that preprocessing and prediction followed a consistent workflow.

Numerical features

* Missing-value imputation
* Standardization using StandardScaler

Categorical features

* Missing-value imputation
* One-hot encoding with support for previously unseen categories

The transformations were combined using ColumnTransformer and integrated directly into the machine learning pipeline.

📊 Model Evaluation

Model performance was evaluated using several classification metrics:

* Accuracy — overall proportion of correct predictions
* Balanced Accuracy — accuracy adjusted for differences in class distribution
* Recall — ability of the model to correctly identify positive instances

Cross-validation was additionally used during hyperparameter optimization to reduce dependence on a single train/test split.

🛠️ Technologies

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* Joblib
* Jupyter Notebook

🚀 Running the Project

Install the required dependencies:

pip install pandas numpy scikit-learn matplotlib seaborn joblib

Then open the notebook using Jupyter Notebook, JupyterLab or Google Colab and execute the analysis sequentially.

The repository also contains the serialized Random Forest model:

P2_RANDOMFORESTmodel.joblib

which can be loaded using Joblib for predictions without retraining the model.

📚 Context

This project was developed as part of a Big Data & Business Analytics course and focuses on applying supervised machine learning techniques to a real-world business classification problem.
