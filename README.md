# Earthquake Prediction Project

This project focuses on predicting earthquake magnitude and depth based on timestamp, latitude, and longitude. The dataset includes historical earthquake data, and a neural network model is trained using Keras to make predictions.

## Project Overview

- **Data Source**: The dataset contains historical earthquake records with attributes such as date, time, latitude, longitude, depth, and magnitude.
- **Data Processing**:
  - Cleaned and filtered the dataset to retain relevant columns: `Date`, `Time`, `Latitude`, `Longitude`, `Depth`, `Magnitude`.
  - Converted the date and time into Unix timestamps for modeling.
  
- **Model**:
  - A Sequential neural network was built with fully connected layers.
  - **Input Features**: `Timestamp`, `Latitude`, and `Longitude`.
  - **Predicted Targets**: `Magnitude` and `Depth`.

- **Visualization**:
  - Used Basemap to plot affected areas of earthquakes globally.
  - Visualized earthquake occurrences using latitude and longitude on a world map.

## Requirements

To run the project, you will need the following libraries:

```bash
pip install numpy pandas matplotlib scikit-learn keras basemap
```

## Model Architecture

The neural network consists of the following layers:

- **Input Layer**: Takes in the features `Timestamp`, `Latitude`, and `Longitude`.
- **Hidden Layers**: Two dense layers with customizable activation functions (`sigmoid` and `relu` used).
- **Output Layer**: A softmax layer predicting both `Magnitude` and `Depth`.
- **Optimizer**: Stochastic Gradient Descent (SGD).
- **Loss Function**: Squared Hinge Loss.
- **Batch Size**: 10.
- **Epochs**: 20.

## Data Split

The dataset was split into training and testing sets using an 80/20 ratio:

- **Training Data**: 80% of the dataset.
- **Testing Data**: 20% of the dataset.

## Model Performance

The model was evaluated on the test data with the following metrics:

- **Test Loss**: 0.5041
- **Test Accuracy**: 97.93%
