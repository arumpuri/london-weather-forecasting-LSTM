# London Weather Time Series Analysis with LSTM

This project focuses on analyzing and forecasting London weather data from 1979 to 2023 using Long Short-Term Memory (LSTM) networks. The dataset includes various meteorological features such as temperature, precipitation, humidity, and sunshine duration, providing a comprehensive view of weather trends and seasonality.

## Table of Contents
- [Dataset](#dataset)
- [Features](#features)
- [Requirements](#requirements)
- [Project Workflow](#project-workflow)
- [Key Results](#key-results)
- [Usage](#usage)
- [Acknowledgments](#acknowledgments)

## Dataset
The dataset contains daily weather data with the following features:
- **DATE:** Date in YYYY-MM-DD format.
- **TX:** Daily maximum temperature (0.1°C).
- **TN:** Daily minimum temperature (0.1°C).
- **TG:** Daily mean temperature (0.1°C).
- **SS:** Daily sunshine duration (0.1 hours).
- **SD:** Daily snow depth (1 cm).
- **RR:** Daily precipitation amount (0.1 mm).
- **QQ:** Daily global radiation (W/m²).
- **PP:** Daily sea level pressure (0.1 hPa).
- **HU:** Daily relative humidity (%).
- **CC:** Daily cloud cover (oktas).

Each parameter includes an associated quality code:
- **0:** Valid data
- **1:** Suspect data
- **9:** Missing data

## Features
- **Data Preprocessing:** Unit conversion, handling missing values, and filtering invalid data.
- **Exploratory Data Analysis (EDA):** Trend, seasonality, and Fourier Transform analysis.
- **Modeling:** LSTM-based model for time series prediction.
- **Visualization:** Predicted vs actual values, residual analysis, and seasonality trends.

## Requirements
Ensure you have the following installed:
- Python 3.8+
- Required Python libraries (install using `requirements.txt`):

```bash
pip install -r requirements.txt
```

### Example `requirements.txt`:
```
numpy
pandas
matplotlib
seaborn
scikit-learn
tensorflow
scipy
```

## Project Workflow
1. **Data Loading:** Import and parse the dataset.
2. **Preprocessing:**
   - Convert units to human-readable formats (e.g., °C, hours).
   - Handle missing values and filter data based on quality codes.
3. **EDA:**
   - Visualize trends and seasonality.
   - Analyze correlations between features.
4. **Feature Engineering:**
   - Create lag features for time series modeling.
   - Aggregate data for seasonality detection.
5. **Modeling:**
   - Split data into training and testing sets.
   - Train LSTM model for forecasting.
6. **Evaluation:**
   - Visualize actual vs predicted values.
   - Compute metrics like MAE, RMSE, and R².
7. **Visualization:**
   - Trend analysis using Fourier Transform.
   - Residual and error distribution plots.

## Key Results
- The LSTM model effectively captures seasonal trends in temperature and precipitation.
- Visualization of actual vs predicted values indicates a close match for short-term forecasting.

## Usage
1. Clone the repository:

```bash
git clone https://github.com/yourusername/london-weather-lstm.git
```

2. Navigate to the project directory:

```bash
cd london-weather-lstm
```

3. Run the main script:

```bash
python main.py
```

4. Modify `config.py` to adjust parameters like LSTM layers, batch size, and epochs.

## Acknowledgments
- The dataset was provided by Kaggle.
- Special thanks to the Python open-source community for libraries used in this project.

Feel free to contribute to this repository by submitting issues or pull requests!
