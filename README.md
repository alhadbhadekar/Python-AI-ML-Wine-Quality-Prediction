﻿# Wine Quality Prediction Using AI/ML

## Overview

This project implements a wine quality prediction model using machine learning techniques in Python. The goal is to classify wines as either "good" or "bad" based on various physicochemical properties.

## Dataset

The dataset used for this project is the **Wine Quality dataset**. It can be downloaded from various sources, including:

[Download winequality-red.csv](https://www.kaggle.com/datasets/uciml/red-wine-quality-cortez-et-al-2009)

### About the Dataset

The dataset contains several attributes related to the physicochemical properties of red wine and the corresponding quality score. Key features include:

- **Fixed Acidity**
- **Volatile Acidity**
- **Citric Acid**
- **Residual Sugar**
- **Chlorides**
- **Free Sulfur Dioxide**
- **Total Sulfur Dioxide**
- **Density**
- **pH**
- **Sulphates**
- **Alcohol**
- **Quality**: Ranges from 0 (bad quality) to 10 (excellent quality)

## Dependencies

Ensure you have the following Python packages installed:

- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn

You can install the required packages using pip:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

## Project Structure

The main code is contained in the `Wine Quality Prediction.ipynb` Jupyter notebook, which includes:

1. **Data Collection**: Loading the dataset into a pandas DataFrame.
2. **Data Exploration**: Inspecting the dataset, checking for missing values, and visualizing distributions.
3. **Correlation Analysis**: Analyzing the correlation between features and the target variable using heatmaps.
4. **Data Preprocessing**: Separating features and labels, and performing label binarization.
5. **Train-Test Split**: Splitting the dataset into training and testing sets.
6. **Model Training**: Training a Random Forest Classifier model.
7. **Model Evaluation**: Evaluating the model's accuracy on the test dataset.
8. **Prediction**: Building a predictive system to classify the quality of wine based on user input.

## Getting Started

1. **Download the Dataset**: Ensure you have the `winequality-red.csv` file in your project directory.

2. **Run the Jupyter Notebook**: Open `Wine Quality Prediction.ipynb` and execute the cells sequentially.

3. **Model Training and Evaluation**: The notebook includes code to train the model and evaluate its accuracy.

## Example Usage

After running the model, you can test predictions using new input data:

```python
input_data = (7.5, 0.5, 0.36, 6.1, 0.071, 17.0, 102.0, 0.9978, 3.35, 0.8, 10.5)

# Changing the input data to a numpy array
input_data_as_numpy_array = np.asarray(input_data)

# Reshape the data for prediction
input_data_reshaped = input_data_as_numpy_array.reshape(1, -1)

# Predicting the wine quality
prediction = model.predict(input_data_reshaped)

if (prediction[0] == 1):
    print('Good Quality Wine')
else:
    print('Bad Quality Wine')
```

## Acknowledgments

- Dataset from the UCI Machine Learning Repository
- Matplotlib and Seaborn for data visualization
- Scikit-learn for machine learning utilities

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Conclusion

This project provides a foundational understanding of using AI/ML for classification tasks. Enjoy experimenting with wine quality predictions!
