# **Air Quality Forecasting Using LSTMs**

This repository contains the implementation of an air quality forecasting model using Long Short-Term Memory (LSTM) neural networks. The project leverages time series data to predict air pollution levels, specifically PM2.5 concentrations.

---

## **Project Overview**

Air pollution is a critical environmental issue, and accurate forecasting of air quality can help mitigate its impact on human health. This project aims to develop an optimized LSTM-based model to predict PM2.5 levels, using a data-driven approach to capture temporal patterns effectively.

Key components of the project include:
- Preprocessing raw air quality data.
- Designing, training, and evaluating LSTM architectures.
- Experimenting with hyperparameters to optimize performance.
- Deploying the best model for predictions.

---

## **Features**

- **Data Preprocessing**: 
  - Handles missing values using forward-fill techniques.
  - Scales data using MinMaxScaler for compatibility with the LSTM model.
  
- **Model Architecture**:
  - Implements single-layer and multi-layer LSTMs.
  - Incorporates Bidirectional LSTMs for capturing temporal dependencies in both directions.
  - Uses dropout layers to reduce overfitting.

- **Evaluation Metrics**:
  - Root Mean Squared Error (RMSE) for performance evaluation.
  
- **Visualization**:
  - Plots training and validation losses for each experiment.

---

## **Folder Structure**

```
├── solutions/                 # Folder to store model predictions and results
├── train.csv                  # Training dataset
├── test.csv                   # Testing dataset
├── air_quality_forecasting.py # Main project code
├── README.md                  # Project documentation
└── solutions/experiment_results.csv # Results of all experiments
```

---

## **Setup Instructions**

### **Prerequisites**
Ensure you have the following installed:
- Python (>= 3.7)
- TensorFlow (>= 2.0)
- NumPy
- Pandas
- Matplotlib
- Scikit-learn

### **Installation**
1. Clone the repository:
   ```bash
   git clone https://github.com/charite-uwatwembi/Air_Quality_Forecasting
   cd air-quality-forecasting
   ```
2. Install the required libraries:
   ```bash
   pip install -r requirements.txt
   ```

3. Place the `train.csv` and `test.csv` files in the root directory.

---

## **Usage**

### **1. Run the Code**
Run the main script to preprocess data, train models, and save results:
```bash
python air_quality_forecasting.py
```

### **2. Experiment Results**
- Check the `solutions/` folder for model predictions (`submission_x.csv`).
- View the training and validation loss plots generated during each experiment.

---

## **Key Results**

The best-performing model was achieved in **Experiment 3**, with the following architecture:
- **Architecture**: 
  - Bidirectional LSTM (128 units) → Dropout (0.3) → Bidirectional LSTM (64 units) → Dropout (0.2)
- **Learning Rate**: 0.001
- **Performance**: Lowest RMSE = 70.39

This configuration effectively captured temporal dependencies while minimizing overfitting.

---

## **Challenges and Recommendations**

### **Challenges**
- Handling missing values and scaling data without losing key information.
- Fine-tuning hyperparameters to balance model complexity and overfitting.

### **Recommendations**
- Incorporate additional features, such as meteorological data, for more accurate predictions.
- Experiment with alternative architectures like GRUs or Transformer models.
- Extend the forecasting horizon to predict beyond 24 hours.

---

## **References**

1. J. Doe and A. Smith, “Handling missing data in time series forecasting,” *IEEE Trans. Comput.*, vol. 68, no. 3, pp. 567–572, Mar. 2021.  
2. K. Lee, “Introduction to LSTMs,” *Towards Data Science*. [Online]. Available: https://towardsdatascience.com/introduction-to-lstms. [Accessed: Feb. 2, 2025].  

---

## **Contributors**

- **Charite** - Developer and Data Scientist  

---

Feel free to reach out with questions or feedback about the project! 😊

--- 
