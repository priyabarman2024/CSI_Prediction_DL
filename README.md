# CSI_Prediction_DL

**Channel State Information (CSI) prediction for Massive MIMO systems** using various deep learning techniques such as **CNN, RNN, LSTM, Transformer**, and hybrid models in Python. This project covers the entire machine learning pipeline: data preprocessing, model training, evaluation, and visualization.

---

##  Project Highlights

-  Multiple models (CNN, RNN, LSTM, Transformer) for comparison
-  Data preprocessing pipeline: encoding, missing value imputation, MinMax scaling
-  Custom PyTorch `Dataset` with sliding windows for temporal modeling
-  Training loop with early stopping and learning rate scheduling
-  Evaluation using MAE, RMSE, and SMAPE
-  Heatmap visualization of prediction performance
-  Optional: Save predicted CSI values for spectral efficiency analysis

---

##  Folder Structure

```
CSI_Prediction_DL/
├── csi-pred1.ipynb            # Main notebook with full pipeline
├── README.md                  # Project documentation
└── requirements.txt           # Python dependencies
```

---

## ⚙️ Installation

1. **Clone the repository**
```bash
git clone https://github.com/priyabarman2024/CSI_Prediction_DL.git
cd CSI_Prediction_DL
```

2. **Install dependencies**
```bash
pip install -r requirements.txt
```

---

## 🗃️ Dataset

Ensure the dataset is available at the following path:
```
/kaggle/input/csi-data/CSI_Data.csv
```

### Preprocessing steps:
- Drop irrelevant columns: `datetime(utc)`, `flycState`, `message`
- Encode categorical variables using LabelEncoder
- Fill missing values with column mean
- Normalize features using MinMaxScaler

---

## 🏋️‍♂️ Training

Call the following function to start model training:

```python
train_model(model, train_loader, val_loader, criterion, optimizer)
```

- Includes early stopping if validation loss doesn't improve
- Uses `ReduceLROnPlateau` for adaptive learning rate reduction

---

## 📈 Evaluation

After training:
- Evaluate performance using MAE, RMSE, and SMAPE
- Visual comparison between actual vs predicted CSI values
- Save predictions using `pickle` for downstream analysis

---

## 📊 Visualization

- Heatmap of prediction performance
- Loss curves (Train vs Validation)
- Error histograms (optional)

---

## 🔮 Future Enhancements

- Implement CSI-to-Spectral Efficiency mapping
- Extend to 5G NR or 6G simulation environments (e.g., NS-3, MATLAB)
- Add model explainability (e.g., SHAP values for time-series)

---

## 👩‍💻 Author

**Priya Barman**  
🔗 [Kaggle Profile](https://www.kaggle.com/priyabarman2024)

---

## 📜 License

This project is licensed under the MIT License.
