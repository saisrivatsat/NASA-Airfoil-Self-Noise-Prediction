# NASA-Airfoil-Self-Noise-Prediction

## **Predicting Airfoil Self-Noise: A Machine Learning and Deep Learning Approach**

## **Project Overview**
This project aims to predict the **Scaled Sound Pressure Level (dB)** of airfoil blade sections based on aerodynamic and acoustic test data collected in a wind tunnel. The objective is to evaluate the effectiveness of **Machine Learning (Linear Regression)** and **Deep Learning (Neural Networks)** models in forecasting noise levels based on various physical parameters.

## **Dataset Description**
The dataset consists of **1503 observations** with the following features:

| Feature | Description |
|---------|------------|
| **Frequency (Hz)** | Frequency of the noise signal |
| **Angle of Attack (°)** | The angle at which air flows over the airfoil |
| **Chord Length (m)** | Length of the airfoil section |
| **Free-stream Velocity (m/s)** | Speed of airflow |
| **Suction Side Displacement Thickness (m)** | Thickness of the suction side boundary layer |
| **Target Variable (dB)** | Scaled sound pressure level (Noise Level) |

## **Objectives**
- Analyze the dataset and preprocess it for modeling.
- Build a **Linear Regression model** as a baseline.
- Develop a **Deep Learning model** using a **Neural Network**.
- Improve the deep learning model by adjusting neurons, adding layers, and changing optimization algorithms.
- Compare the performance of different models using **Mean Squared Error (MSE).**

## **Methodology**
### **1. Data Preprocessing**
- Load the dataset (tab-separated format) and check for missing values.
- Normalize the features to improve model performance.
- Split the data into **80% training** and **20% testing** sets.

### **2. Model Development**
#### **Linear Regression Model**
- Used as a baseline to compare with deep learning models.
- Achieved a test **MSE of 22.1286**.

#### **Deep Learning Models**
- Built a simple **2-layer neural network** using TensorFlow/Keras.
- Initially performed **worse than Linear Regression (MSE: 26.2215)**.
- Increased neurons in the hidden layer, improving performance to **MSE: 22.8996**.
- Added more layers, reducing MSE to **18.7831**, demonstrating the benefits of deeper networks.
- Used **RMSprop optimizer**, but results remained similar (MSE: 18.9457).

## **Key Results**
| Model | Test MSE |
|--------|----------------|
| **Linear Regression** | 22.1286 |
| **Basic Deep Learning Model** | 26.2215 |
| **More Neurons Model** | 22.8996 |
| **More Layers Model** | **18.7831** |
| **RMSprop Optimizer Model** | 18.9457 |

## **Insights & Business Impact**
- **Deeper neural networks significantly improved performance** over linear regression.
- **Adding layers was more effective than increasing neurons**, highlighting the need for complex architectures in aerodynamic modeling.
- **Optimizer choice had minimal impact**, indicating that architecture tuning is more critical.

## **Future Improvements**
- **Hyperparameter tuning** using grid search for better optimization.
- **Regularization techniques** to prevent overfitting.
- **Feature engineering** to explore additional predictive variables.
- **Deployment of the best model** for real-time predictions in aerospace applications.

## **Conclusion**
This study successfully demonstrated how deep learning can **enhance predictive modeling** for aerodynamic noise analysis. By leveraging **neural network architectures**, we achieved **a significant reduction in error** compared to traditional machine learning methods. This approach can be further refined to aid **aircraft design and noise reduction strategies**, supporting the development of **quieter and more efficient airfoil technologies**.

---

- **Tools Used:** Python, Pandas, NumPy, Scikit-learn, TensorFlow/Keras, Matplotlib
