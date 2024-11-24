# 🎙️ **Gender Recognition by Voice Using SVM**

This project focuses on gender recognition based on voice features using **Support Vector Machine (SVM)**. We use different kernels and fine-tune the hyperparameters to achieve the best performance in classifying voices as either male or female. The dataset consists of 3,168 samples, with an equal number of male and female voices (1,584 each). 

---

## 📋 **Dataset Overview**

- **Total number of samples:** 3,168  
- **Male voices:** 1,584  
- **Female voices:** 1,584  

The dataset includes 21 features per voice sample, which are used to train the **SVM classifier** to predict gender.

---

## 🧑‍💻 **Modeling with Support Vector Machine (SVM)**  

1. **SVM with Different Kernels:**  
   We explored **four different kernels** for the SVM model:
   - **Linear kernel**
   - **Radial Basis Function (RBF) kernel**
   - **Polynomial kernel**  

   The default performance with each kernel was evaluated:

   - **Default SVM (no tuning):** 97.6% accuracy  
   - **Linear kernel:** 97.7% accuracy  
   - **RBF kernel:** 97.6% accuracy  
   - **Polynomial kernel:** 95.8% accuracy  

---

## 🔄 **K-Fold Cross-Validation**

We performed **K-fold cross-validation** with different kernels to better evaluate the model's generalization capability:

- **Linear kernel:** 97.9% accuracy  
- **RBF kernel:** 96.5% accuracy  
- **Polynomial kernel:** 94.5% accuracy  

From the K-fold cross-validation, we can see that the **linear kernel** performed the best, with the highest accuracy.

---

## ⚙️ **Hyperparameter Tuning**

Next, we tuned the following hyperparameters to further optimize the model:

1. **Polynomial kernel with different degrees:**  
   We experimented with different degrees of the polynomial kernel, but the performance remained at **95.8%** with degree 3.

2. **SVM with different hyperparameters:**  
   - **C=0.1, Linear kernel:** Achieved **97.4%** accuracy  
   - **Gamma=0.01, RBF kernel:** Achieved **96.8%** accuracy  
   - **Degree=3, Polynomial kernel:** Achieved **95.8%** accuracy  

---

## 🔍 **Grid Search for Best Hyperparameters**

Using **grid search** to find the best hyperparameters, we achieved an accuracy of **96%**. The grid search considered multiple values of **C**, **gamma**, and **degree** to identify the optimal parameters.

---

## 🎯 **Results**

- **SVM Default Parameters:** 97.6%  
- **Linear Kernel:** 97.7%  
- **RBF Kernel:** 97.6%  
- **Polynomial Kernel:** 95.8%  
- **K-Fold Cross-Validation Results:**  
  - Linear kernel: 97.9%  
  - RBF kernel: 96.5%  
  - Polynomial kernel: 94.5%  
- **Hyperparameter Tuning Results:**  
  - **C=0.1, Linear kernel:** 97.4%  
  - **Gamma=0.01, RBF kernel:** 96.8%  
  - **Degree=3, Polynomial kernel:** 95.8%  
- **Grid Search:** 96%  

---

## 🧰 **Tools and Techniques**  

- **Libraries Used:** `pandas`, `NumPy`, `scikit-learn`  
- **Model:** **Support Vector Machine (SVM)**  
- **Kernels Tested:** Linear, RBF, Polynomial  
- **Hyperparameter Tuning:** Grid Search for best parameters

---

## 🌟 **Key Takeaways**  

- The **linear kernel** performed the best for this gender recognition task.
- **K-Fold Cross-Validation** is crucial to ensure that the model is not overfitting and generalizes well to unseen data.
- **Hyperparameter tuning** helps optimize model performance, though the default settings with the linear kernel already provided excellent accuracy.
- **Grid Search** further enhances the model's ability to achieve an optimal configuration.
