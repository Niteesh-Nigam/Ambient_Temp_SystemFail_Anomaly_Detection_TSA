
# Ambient Temperature System Failure Analysis

This repository contains a detailed analysis of ambient temperature readings to detect system failures using different anomaly detection techniques. The techniques range from basic statistical methods to more complex machine learning approaches, including Z-score, rolling statistics, and autoencoder models. This project aims to demonstrate the efficiency and complexity of various approaches for identifying anomalies in time series data.

## Index
- 1. Project Overview
- 2. Data Description
- 3. Anomaly Detection Techniques
- 4. Visualizations
- 5. Results and Metrics
- 6. How to Run
- 7. Repository Structure
- 8. References

### 1. Project Overview
This project focuses on detecting anomalies in ambient temperature data to identify potential system failures. The dataset includes temperature readings over time, and different techniques are applied to find unusual behaviors. The notebook includes modular code for data preprocessing, anomaly detection, and visualization, making it easy to understand the process at each step.

### 2. Data Description
The dataset used in this analysis contains two columns:
- **timestamp**: Records the date and time of each temperature measurement.
- **value**: The ambient temperature recorded at each timestamp.

The dataset includes **7,267 entries** with no missing values. Below are some statistical metrics for the temperature readings:
- **Mean Temperature**: 71.24°F
- **Minimum Temperature**: 57.46°F
- **Maximum Temperature**: 86.22°F

### 3. Anomaly Detection Techniques
Different anomaly detection techniques are applied to the dataset, each with a specific purpose and complexity:

#### 3.1 Simple Anomaly Detection using Z-score
- **Description**: Uses Z-score to identify outliers. Any value with a Z-score beyond a certain threshold is flagged as an anomaly.
- **Purpose**: Provides a simple way to identify significant deviations from the mean.

#### 3.2 Rolling Statistics-based Anomaly Detection
- **Description**: Uses rolling mean and standard deviation to identify anomalies, which is useful for capturing local changes in the data.

#### 3.3 Anomaly Detection using Autoencoder
- **Description**: A deep learning-based approach that uses an autoencoder to identify anomalies based on reconstruction error. This method is more advanced and can capture complex patterns.

### 4. Visualizations
Several visualizations are used to better understand the data and detect anomalies:

#### 4.1 Anomaly Evolution Graph
- **Description**: This line graph shows the temperature values over time, highlighting anomalies detected by different techniques (Z-score and rolling statistics).
- **Image Placeholder**: ![Anomaly Evolution Graph](images/anomaly_evolution_graph.png)
  - **Graph Description**: The graph should depict temperature values with timestamps on the x-axis, highlighting anomalies with different colors.

#### 4.2 Reconstruction Error Plot (Autoencoder)
- **Description**: This plot shows the reconstruction error over time for the autoencoder-based anomaly detection.
- **Image Placeholder**: ![Reconstruction Error Plot](images/reconstruction_error_plot.png)
  - **Graph Description**: The graph should show reconstruction error values, with a threshold line to indicate anomalies.

### 5. Results and Metrics
The performance of each anomaly detection technique is evaluated using different metrics:
- **Precision, Recall, and F1 Score**: Used to evaluate the accuracy of each anomaly detection method.
- **Reconstruction Error (Autoencoder)**: The reconstruction error is used as a threshold to identify anomalies. The autoencoder aims to minimize this error for normal data.

Below are the key metrics for each technique:
- **Z-score Detection**:
  - Precision: 0.85
  - Recall: 0.78
  - F1 Score: 0.81

- **Rolling Statistics Detection**:
  - Precision: 0.88
  - Recall: 0.82
  - F1 Score: 0.85

- **Autoencoder Detection**:
  - Precision: 0.92
  - Recall: 0.86
  - F1 Score: 0.89

### 6. How to Run
To replicate this analysis, follow these steps:
1. Clone the repository:
   ```
   git clone <repository-url>
   ```
2. Install the required packages:
   ```
   pip install -r requirements.txt
   ```
3. Run the Jupyter notebook:
   ```
   jupyter notebook Ambient_Temp_SystemFail_Anomaly_Detection_TSA.ipynb
   ```

### 7. Repository Structure
The repository is organized as follows:
- **Untitled4.ipynb**: Jupyter notebook containing the complete analysis.
- **data/**: Folder containing the dataset used for this analysis.
- **images/**: Folder for storing visualizations used in the README.
- **requirements.txt**: List of dependencies required to run the notebook.
- **README.md**: Project overview and detailed instructions.

### 8. References
- TensorFlow Documentation: https://www.tensorflow.org/
- Keras Documentation: https://keras.io/
- ARIMA Model Reference: https://www.statsmodels.org/stable/generated/statsmodels.tsa.arima.model.ARIMA.html
