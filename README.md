# Big Data Processing: Stroke Prediction (Random Forest vs Naive Bayes)

This project was developed as a **final assignment** for the **Big Data Processing** course at **BINUS University**.  
We compared the performance of two machine learning models — **Random Forest** and **Naive Bayes** — to predict stroke occurrence based on patient health data.

---

## Team Members
- **Ferlie Hernata** – 2702231262  
- Giovincent Ricel’s Tanoto – 2702226786  
- Josh Nicholas Sutanto – 2702234825  
- Nikolaus Marvin Liayasa – 2702233702  
- Rendy Riady – 2702234421  
- Matthew Ethan Laurent – 2702231496  

---

## Dataset
- **Name:** Brain Stroke Dataset  
- **Source:** [Kaggle – Jillani SofTech](https://www.kaggle.com/datasets/jillanisofttech/brain-stroke-dataset)  
- **Features:** Age, gender, hypertension, heart disease, BMI, smoking status, etc.  
- **Target:** Stroke (1 = yes, 0 = no)

---

## Workflow
1. **Data Collection** – Dataset downloaded from Kaggle API.  
2. **Data Preparation & EDA** – Data inspection, univariate & bivariate analysis, correlation heatmap.  
3. **Data Splitting** – 80:20 train-test split using scikit-learn.  
4. **Handling Imbalanced Data** – Applied **SMOTE** to oversample minority class (stroke cases).  
5. **Model Building** – Trained two models:
   - Random Forest Classifier
   - Gaussian Naive Bayes
6. **Model Evaluation** – Compared metrics: Accuracy, Precision, Recall, F1-score.
7. **Visualization** – Bar charts to visualize performance comparison.

---

## Results

| Model          | Accuracy | Precision | Recall | F1-Score |
|----------------|----------|----------|--------|----------|
| **Random Forest** | **0.9147** | 0.5015 | 0.5010 | 0.5002 |
| **Naive Bayes**   | 0.5707 | 0.5489 | **0.7381** | 0.4487 |

- **Random Forest** achieved the highest **accuracy** (91.47%) but had low recall, meaning it often failed to detect minority class (stroke cases).  
- **Naive Bayes** had higher **recall** (73.81%), making it more sensitive to stroke detection, but had poor overall accuracy.  

### Key Insights:
- **Random Forest** is better for overall stability but needs improvement in minority class detection.
- **Naive Bayes** is more sensitive but misclassifies too many non-stroke cases.
- SMOTE helped balance the training data but class imbalance in the test set remains a challenge.

---

## Report & Notebook
-  [Jupyter Notebook](./Final_Project_BDP_Group4_.ipynb)  
-  [Final Report (PDF)](./Perbandingan%20Kinerja%20Model%20Random%20Forest%20dan%20Naive%20Bayes%20dalam%20Prediksi%20Stroke.pdf)

---

## Future Work
- Try feature engineering for better class separation.
- Experiment with **XGBoost** or **LightGBM** for improved recall.
- Consider **threshold tuning** or **cost-sensitive learning** to handle imbalanced data more effectively.
