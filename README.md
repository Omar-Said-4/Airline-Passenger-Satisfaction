# ✈️ Airline Passenger Satisfaction Prediction  
> A Machine Learning Application.

## 🧾 Table of Contents
- [📌 Project Overview](#project-overview)
- [📂 Dataset](#dataset)
- [🧹 Data Preprocessing](#data-preprocessing)
- [🤖 Models Implemented](#models-implemented)
  - [🔹 Logistic Regression](#1-logistic-regression)
  - [🔹 Random Forest](#2-random-forest)
  - [🔹 AdaBoost with Logistic Regression](#3-adaboost-with-logistic-regression)
  - [🔹 AdaBoost with Decision Trees](#4-adaboost-with-decision-trees)
- [📈 Key Findings](#key-findings)
- [✍️ Contributors](#️-contributors)

---

## 📌 Project Overview
<a name="project-overview"></a>  
**Problem:**  
Predict airline passenger satisfaction levels based on survey data to help airlines improve their services.

---

## 📂 Dataset
<a name="dataset"></a>  
[📄 Dataset Link](https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction?select=train.csv)

---

## 🧹 Data Preprocessing
<a name="data-preprocessing"></a>  
1. **Handling Missing Values:**
   - Identified NULL values  
   - Used `IterativeImputer` to estimate them

2. **Feature Correlation:**
   - Visualized correlations using a heatmap  
   - Removed highly correlated features

3. **Outlier Removal:**
   - Used Mahalanobis distance with chi-square threshold (95th percentile)

---

## 🤖 Models Implemented
<a name="models-implemented"></a>  
### 🔹 1. Logistic Regression
<a name="1-logistic-regression"></a>  
- L2 regularization with `max_iter=10000`  
- Tuned inverse regularization strength (`C`)  
- 5-fold cross-validation  
- **Results:**  
  - Training F1-score: `0.88`  
  - Testing F1-score: `0.87`

### 🔹 2. Random Forest
<a name="2-random-forest"></a>  
- Parameters: `max_depth=20`, `min_samples_leaf=5`, `class_weight='balanced'`  
- Tuned number of estimators  
- Used 5-fold cross-validation

### 🔹 3. AdaBoost with Logistic Regression
<a name="3-adaboost-with-logistic-regression"></a>  
- Base estimator: `LogisticRegression(max_iter=1000)`  
- Tuned number of estimators and learning rate  
- **Results:**  
  - Training F1-score: `0.93`  
  - Testing F1-score: `0.93`

### 🔹 4. AdaBoost with Decision Trees
<a name="4-adaboost-with-decision-trees"></a>  
- Tested decision stumps and trees (`max_depth=6`)  
- **Results:**  
  - Decision stumps F1-score: `0.93`  
  - Deeper trees (`max_depth=6`) F1-score: `0.96`

---

## 📈 Key Findings
<a name="key-findings"></a>  
- **Non-linear models outperformed linear models**, suggesting complex relationships in the data  
- **Top Important Features:**
  1. ⏱️ Departure/Arrival time convenience  
  2. 💺 Seat comfort  
  3. 🧳 Type of Travel (Business/Personal)  
  4. 🍽️ Food and drink quality  
  5. 🧑‍✈️ On-board service

---

## ✍️ Contributors
<a name="contributors"></a>  
<table>
  <tr>
    <td align="center">
      <a href="https://github.com/Omar-Said-4" target="_blank">
        <img src="https://avatars.githubusercontent.com/u/87082462?v=4" alt="Omar Said"/>
        <br />
        <sub><b>Omar Said</b></sub>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/MostafaMagdyy" target="_blank">
        <img src="https://avatars.githubusercontent.com/u/97239596?v=4" alt="Mostafa Magdy"/>
        <br />
        <sub><b>Mostafa Magdy</b></sub>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/nouraymanh" target="_blank">
        <img src="https://avatars.githubusercontent.com/u/102790603?v=4" alt="Nour Ayman"/>
        <br />
        <sub><b>Nour Ayman</b></sub>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/3abqreno" target="_blank">
        <img src="https://avatars.githubusercontent.com/u/102177769?v=4" alt="Abdelrahman Mohamed"/>
        <br />
        <sub><b>Abdelrahman Mohamed</b></sub>
      </a>
    </td>
  </tr>
</table>
