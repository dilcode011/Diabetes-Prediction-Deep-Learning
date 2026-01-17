#  Diabetes Prediction with Keras Tuner

##  Project Overview
This project demonstrates a Deep Learning approach to predict whether a patient has diabetes based on diagnostic measurements. 

Unlike standard implementations, this project utilizes **Keras Tuner** to perform hyperparameter optimization. The model doesn't just use fixed settings; it programmatically searches for the best combination of layers, neurons, and learning rates to maximize prediction accuracy.

##  The Dataset
The model is trained on the **Pima Indians Diabetes Dataset**.
**Input Features:**
* `Pregnancies`: Number of times pregnant
* `Glucose`: Plasma glucose concentration
* `BloodPressure`: Diastolic blood pressure (mm Hg)
* `SkinThickness`: Triceps skin fold thickness (mm)
* `Insulin`: 2-Hour serum insulin (mu U/ml)
* `BMI`: Body mass index
* `DiabetesPedigreeFunction`: Diabetes pedigree function
* `Age`: Age (years)

**Target:**
* `Outcome`: 0 (No Diabetes) or 1 (Diabetes)

##  Tech Stack
* **Python**
* **TensorFlow / Keras** (Deep Learning Architecture)
* **Keras Tuner** (Hyperparameter Optimization)
* **Pandas & NumPy** (Data Handling)
* **Scikit-Learn** (Preprocessing & Standard Scaling)

##  Key Technical Features
1.  **Data Preprocessing:** * Features are standardized using `StandardScaler` to ensure the neural network converges faster.
    * Data is split into training and testing sets (80/20 split).
2.  **Hyperparameter Tuning (RandomSearch):**
    The project uses `keras-tuner` to automate the selection of:
    * **Model Depth:** Dynamically tests between 1 to 10 hidden layers.
    * **Neurons:** Searches for the optimal number of units (8 to 128) per layer.
    * **Optimizers:** Experiments with `Adam`, `SGD`, `RMSprop`, etc.
    * **Regularization:** Tests different Dropout rates (0.1 - 0.9) to prevent overfitting.

##  Installation & Usage
1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/YOUR_USERNAME/Diabetes-Prediction-Deep-Learning.git](https://github.com/YOUR_USERNAME/Diabetes-Prediction-Deep-Learning.git)
    cd Diabetes-Prediction-Deep-Learning
    ```

2.  **Install dependencies:**
    ```bash
    pip install pandas numpy tensorflow keras-tuner scikit-learn
    ```

3.  **Run the Notebook:**
    Open `Diabetes_prediction_keras_tuner.ipynb` in Jupyter Notebook or Google Colab to see the training process and the tuner results.

## 📊 Results
* The Keras Tuner successfully identified the optimal hyperparameters.
* The final model achieves a validation accuracy of approximately **76% - 80%**.

