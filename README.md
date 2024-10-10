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
