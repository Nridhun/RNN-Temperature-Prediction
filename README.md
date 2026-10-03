
# RNN Temperature Prediction

This project uses a Recurrent Neural Network (RNN) to predict temperature from historical weather data.

## Project Overview

The dataset contains hourly weather observations. The data was converted into daily data and prepared for time-series prediction.

The RNN uses the following weather features:

- Humidity
- Wind Speed
- Pressure

The target variable is:

- Temperature

A 7-day time sequence is used to predict the next day's temperature.

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- TensorFlow
- Keras
- Jupyter Notebook

## Project Workflow

1. Load the weather dataset
2. Explore and clean the data
3. Convert hourly data into daily data
4. Check for missing values
5. Select input features and target
6. Scale the data using MinMaxScaler
7. Split the data into training and testing sets
8. Create 7-day sequences for the RNN
9. Build a Simple RNN model
10. Train the model
11. Evaluate the model
12. Visualize actual vs predicted temperatures

## RNN Model

The model consists of:

- SimpleRNN layer with 50 units
- Tanh activation function
- Dense output layer
- Adam optimizer
- Mean Squared Error (MSE) loss

The model uses the previous 7 days of weather information to predict temperature.

## Model Performance

The model was evaluated using the test dataset.

| Metric | Result |
|---|---:|
| MAE | 4.17°C |
| MSE | 28.81 |
| R² Score | 0.59 |

The model was able to learn the general temperature pattern, although some sudden temperature changes were not predicted accurately.

## Results

The project includes:

- Training and validation loss graph
- Actual vs predicted temperature graph

The prediction graph shows that the RNN generally follows the overall pattern of the actual temperature.

## Project Structure

```text
RNN-Temperature-Prediction/
│
├── RNN_Temperature_Prediction.ipynb
├── README.md
└── dataset.csv
