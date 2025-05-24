# CSI_Prediction_DL
Channel State Information (CSI)  prediction for Massive MIMO system using different types of Deep Learning techniques like CNN, RNN, LSTM, Transformer and also hybrid models in Python. Includes data preprocessing, feature engineering, model training, and evaluation using metrics like MAE, RMSE, SMAPE and also include heatmap visualization.

## Project highlights
- Different model to compare the resilts.
- Data preprocessing pipeline: encoding, missing value imputation, scaling.
- Custom PyTorch Dataset with sliding windows.
- Training with early stopping and learning rate scheduling.
- Evaluation using MSE & MAE.
- visualization with heatmap.
- Optionally save predicted CSI for spectral efficiency analysis.
- 
##  Folder Structure
CSI_Prediction_DL/
├── csi-pred1.ipynb # Main notebook with code
├── README.md # Project documentation
└── requirements.txt # Python dependencies

##  Installation
1.Clone this repository:
git clone https://github.com/priyabarman2024/CSI_Prediction_DL.git
cd CSI_Prediction_DL
2.Install dependencies:
pip install -r requirements.txt

## Dataset
/kaggle/input/csi-data/CSI_Data.csv

## Preprocessing includes:
Dropping irrelevant columns (datetime(utc), flycState, message)
Label encoding for categorical features
Mean imputation for missing values
MinMax scaling for numerical stability

## Training
Train the model with:
train_model(model, train_loader, val_loader, criterion, optimizer)
Automatic early stopping and learning rate adjustment using ReduceLROnPlateau.

## Evaluation
After training:
Evaluate on test set using MSE and MAE
Compare predicted vs actual CSI
Save predictions using pickle if needed

## Future enhancements
Implement spectral efficiency calculations
Visualize prediction accuracy across time
Real-time deployment in wireless simulators (e.g., NS-3, MATLAB 5G toolbox)

## Author
Priya Barman


