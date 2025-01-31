# 🧠 Neural Network Implementation & Evaluation  

## 📜 Overview  
This project involves modifying the **NNDL book's "network.py"** code (Chapter 1) to improve its functionality and performance. The goal is to deepen the understanding of neural networks by implementing **evaluation metrics, efficiency improvements, and visualization techniques**.  

## 🎯 Objectives  
- Modify the **network definition code** to include additional evaluation metrics.  
- Optimize **SGD, backpropagation, and mini-batch updates** for efficiency.  
- Implement **early stopping** based on accuracy and MSE loss trends.  
- Develop a **custom test application** to validate the modified network.  
- Visualize **training performance metrics** (Accuracy, MSE, CE, and Log-Likelihood).  

📌 **Dataset**: The **Iris dataset** (iris-3.csv) is used for training and testing.  

## ⚙️ Installation & Dependencies  
### **Requirements**  
- **Python 3.x**  
- **Jupyter Notebook**  
- **Required Libraries**:  
  - `numpy` – Matrix computations  
  - `matplotlib` – Data visualization  
  - `pandas` – Dataset handling  
  - `scipy` – Scientific computations  

## 🔍 Project Structure
### 1️⃣ Initial Setup & Testing
📌 **Objective**: Ensure environment compatibility and run baseline tests.

### 2️⃣ Modifications to the Network Code
📌 **Objective**: Extend the existing evaluate(), SGD(), backprop(), and update_mini_batch() functions.

✅ **Key Modifications**:
- **evaluate() function**: Compute and return
  - ✅ Correctly classified instances (Count)
  - ✅ Accuracy (Accuracy)
  - ✅ Mean Squared Error (MSE)
  - ✅ Cross-Entropy (CE)
  - ✅ Log-Likelihood (LL)
- **SGD() function**:
  - Include **test data evaluation** in a similar format.
  - Implement **early stopping** if accuracy reaches **1.0** or **MSE stops decreasing** (checks last three epochs for stagnation).
  - Return **training and test performance metrics** as nested lists [train_results, test_results].
- **backprop() function**:
  - Preallocate activation matrices for **all layers** to improve efficiency.
- **update_mini_batch() function**:
  - Optimize weight updates by accumulating gradients **without redundant memory allocations.**

### 3️⃣ Testing & Validation
📌 **Objective**: Verify the correctness of the modified network.

✅ **Steps**:
- Run the second test application.
- Ensure it works with a **deeper network** (iris4-20-7-3.dat).

### 4️⃣ Custom Test Application & Visualization
📌 **Objective**: Implement and visualize a new test case.
- Given graphs here are using eta = 0.315, so eta 0.3 should yields consistent results on the performances of both train and test sets. From the graphs, Accuracy increases over time, at epoch 100, trainset yields 98.10% and test set yields 93.33%. Mean-Squared Error, Cross Entropy and Log Likelihood are decreasing over time and both train and test sets.
- Around epoch 60th forward, errors on testing data are slightly higher than training data but not significant. The two lines are almost overlap indicates there is no underfitting/overfitting of the data using eta approximately 0.3. The neural network is performing well on unseen data, correctly classifying the three Iris species.
![Neural Network](https://github.com/pngo1997/Images/blob/main/Neural%20Network.png)  

## 📊 Results & Findings
✅ Successfully extended the evaluation metrics (Accuracy, MSE, CE, LL).

✅ Optimized backpropagation and mini-batch processing for better efficiency.

✅ Implemented early stopping based on accuracy and loss trends.

✅ Verified correctness using multiple test cases.

✅ Created visualizations for training progress.
