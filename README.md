# Multivariate Time Series Forecasting for Air Pollution using LSTMs
This repository provides the code to develop an ***LSTM*** model for ***multivariate time series forecasting*** to predict the pollution at the current hour ***(t)*** given the pollution measurement and weather conditions at the prior time step.
## Requirements
- `numpy`
- `pandas`
- `matplotlib`
- `scikit-learn`
- `keras`
## Usage
### Data
- A dataset that reports on the weather and the level of pollution each hour for five years is being used here that includes the date-time, the pollution called PM2.5 concentration, and the weather information including dew point, temperature, pressure, wind direction, wind speed and the cumulative number of hours of snow and rain.
- Please ensure to save `raw.csv` file given in the `Data` folder in the main data directory and run `Data.py` which preprocesses the data, appropriate for stabilized training of the ***LSTM*** model, and then creates a new data file named `pollution.csv` in the same directory.
### Model Building and Training
- To train the ***LSTM*** model on merely single previous time step window setting and test it in the same setting, run `Train_On_Single_Lag_Timesteps.py`
- To train the ***LSTM*** model on multiple previous time steps, run `Train_On_Multiple_Lag_Timesteps.py`
- All hyperparamters to control training and testing of the model in single as well as multiple time step window settings are provided in their respective `.py` files.
- The average and validation set losses are printed after every epoch.
## Results
| Line Plots of Air Pollution Time Series        | Performance of the *LSTM* model on Single Lag Timesteps Example           | Performance of the *LSTM* model on Multiple Lag Timesteps Example           |
| ------------------------- |:----------------------------:|:---------------------------:|
| ![alt text](https://github.com/fork123aniket/Multivariate-Time-Series-Forecasting-for-Air-Pollution-using-LSTMs/blob/main/Images/1.PNG) | ![alt text](https://github.com/fork123aniket/Multivariate-Time-Series-Forecasting-for-Air-Pollution-using-LSTMs/blob/main/Images/2.PNG) | ![alt text](https://github.com/fork123aniket/Multivariate-Time-Series-Forecasting-for-Air-Pollution-using-LSTMs/blob/main/Images/3.PNG) |
