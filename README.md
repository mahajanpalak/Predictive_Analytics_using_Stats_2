# Learn Probability Density Functions using a Roll-Number-Based Non-Linear Model

## 1. Methodology

The overall workflow followed in this assignment is illustrated below. It shows the sequence from data acquisition to probability density estimation and result analysis.

<img width="848" height="206" alt="Methodology Diagram" src="https://github.com/user-attachments/assets/a6e8f7ce-32a7-4b3f-a50d-ca54998e9bf1" />

---

## 2. Project Description

### a. Data Collection  
An air quality dataset containing nitrogen dioxide (NO₂) concentration values was obtained from Kaggle. This dataset provides real-world environmental data required for the analysis.

### b. Data Pre-processing  
The dataset was pre-processed by removing missing, invalid, and inconsistent values. The NO₂ feature was then selected and transformed using a non-linear function whose parameters depend on the university roll number.

### c. Probability Density Function Parameter Estimation  
A Gaussian-shaped probability density function was assumed for the transformed variable. The parameters μ (mean), λ (precision), and c (normalization constant) were estimated using statistical estimation techniques based on the transformed data.

### d. Density Evaluation  
Using the learned parameters, the probability density function was evaluated for the transformed NO₂ values in order to model their underlying distribution.

### e. Result Interpretation  
The estimated parameters were analyzed, and the resulting probability density function was visualized to verify whether the model appropriately captures the distribution of the transformed data.

---

## 3. Input and Output Flow

**Input:**
- NO₂ concentration values from the dataset (x)
- University roll number (r)

**Processing Steps:**
- Compute transformation parameters  
  - aᵣ = 0.05 × (r mod 7)  
  - bᵣ = 0.3 × (r mod 5 + 1)
- Apply the non-linear transformation  
  - z = x + aᵣ sin(bᵣ x)
- Use the transformed values as input to the PDF model
- Estimate PDF parameters (λ, μ, c) using an estimation method
- Compute the predicted probability density p̂(z)

**Output:**
- Estimated parameters: λ, μ, c  
- Predicted probability density values p̂(z)

---

## 4. Live Notebook Link

The complete implementation and results can be accessed through the following Google Colab notebook:
https://colab.research.google.com/drive/14QLGwyi1KnWi2P3d_dV23KgWtyCA9Wuo?usp=sharing

---

## 5. Sample Output Screenshot

A sample output generated during execution is shown below:

<img src="screenshots/Screenshot%202026-02-04%20212710.png" width="500">
