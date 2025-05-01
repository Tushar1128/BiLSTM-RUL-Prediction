 BiLSTM-RUL-Prediction

Predictive maintenance using Bidirectional LSTM (BiLSTM) to estimate the Remaining Useful Life (RUL) of aircraft engine compressors based on NASA’s C-MAPSS dataset.

 📌 Overview

This project aims to improve the reliability and efficiency of aircraft maintenance by predicting engine failure in advance. It uses a deep learning approach—BiLSTM—to analyze multivariate time-series data and accurately forecast RUL. By leveraging both past and future context, BiLSTM outperforms traditional unidirectional LSTM models in modeling degradation trends.

🚀 Objectives

- Predict Remaining Useful Life (RUL) of aircraft engines using sensor data.
- Compare LSTM and BiLSTM model performance.
- Improve maintenance scheduling and reduce unexpected failures.
- Explore deployment readiness and model robustness in real-world aviation systems.

🧠 Dataset

NASA C-MAPSS FD001
- Contains multivariate time-series sensor readings from simulated turbofan engines.
- Includes 21 sensors, 3 operational settings, engine ID, and cycle count.
- Publicly available: [NASA C-MAPSS Data](https://data.nasa.gov/dataset/C-MAPSS-Dataset/sjf8-pvui)

⚙️ Features Selected

From the original 21 sensors, selected key features include:
- s2 (Fan Inlet Pressure)
- s3 (LPC Outlet Temperature)
- s7, s11, s13, s14 (Various core temps & speeds)
- Operational settings: throttle, altitude, and speed

 🧰 Tech Stack

- Language: Python
- Libraries: TensorFlow/Keras, NumPy, Pandas, Matplotlib, Seaborn, Scikit-learn
- Environment: Jupyter Notebook / Google Colab (with GPU support)

🏗️ Model Architecture

- Input shape: `(60, 25)` sequences
- Two BiLSTM layers: 100 and 60 units
- Dropout layers (30%) for regularization
- Dense output layer (1 neuron, linear activation)
- Loss: Mean Squared Error (MSE)
- Optimizer: RMSprop

📈 Performance Metrics

| Metric   | Value         |
|----------|---------------|
| MAE      | 10.05 cycles  |
| RMSE     | 16.16 cycles  |
| R² Score | 0.8445        |
| F1 Score | 0.9388        |


📄 Report

The complete technical report is available in the `report/` folder, detailing the background, methodology, model architecture, training process, and results.

🔮 Future Work

- Integrate attention mechanisms or Transformer models.
- Enhance interpretability with Explainable AI (XAI) techniques.
- Real-time deployment in cloud or edge computing environments.
- Generalize to other subsets of C-MAPSS (FD002–FD004).

👩‍💻 Authors

- Ankita M – Mechanical Engineering  
- Monica A S – Aerospace Engineering  
- Tushar M – Aerospace Engineering  
- Nikhitha Sunil – Industrial Engineering  

Mentor: Dr. Keshav M, Dept. of Mechanical Engineering, RVCE

 📜 License

This project is licensed under the MIT License. See the `LICENSE` file for details.

