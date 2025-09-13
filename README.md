
# 🩺 ML DOCTOR(Disease Prediction and Recommendation System)

This project is a **machine learning-based disease prediction system** with an integrated **Flask web application**.
It allows users to input their symptoms and get predictions about possible diseases, along with **precautions, medications, workouts, and diet recommendations**.

The system was first built in **Google Colab (IPYNB Notebook)** for data preprocessing, model training, and evaluation, and later deployed using **Flask + HTML frontend (PyCharm IDE)**.

---

##   Features

*   Predicts diseases based on user-entered symptoms
*   Uses multiple ML classifiers (SVC, Random Forest, Gradient Boosting, KNN, Naive Bayes)
*   Achieved **100% accuracy** on the test dataset
*   Flask-based web interface with `index.html` frontend
*   Provides:

  * Disease Description
  * Precautions
  * Medications
  * Recommended Workouts
  * Suggested Diets

---

## 📂 Project Structure

```
├── datasets/
│   ├── Training.csv
│   ├── symptoms_df.csv
│   ├── precautions_df.csv
│   ├── workout_df.csv
│   ├── description.csv
│   ├── medications.csv
│   └── diets.csv
│
├── models/
│   └── svc.pkl   # Trained Support Vector Classifier model
│
├── templates/
│   └── index.html   # Frontend interface
│
├── main.py          # Flask app
├── notebook.ipynb   # Google Colab file for training & testing
├── requirements.txt # Dependencies
└── README.md
```

---

##   Tech Stack

* **Python** (Flask, Pandas, NumPy, Scikit-learn, Pickle)
* **Frontend**: HTML (Flask `render_template`)
* **ML Models Used**:

  * Support Vector Classifier (selected final model ✅)
  * Random Forest
  * Gradient Boosting
  * K-Nearest Neighbors
  * Multinomial Naive Bayes

---

##  Model Training

1. Loaded dataset (`Training.csv`) with **4920 rows × 133 columns**
2. Encoded labels (`prognosis`) using **LabelEncoder**
3. Split dataset: **70% training, 30% testing**
4. Trained multiple classifiers → All achieved **100% accuracy** on test data
5. Final model chosen: **SVC (linear kernel)**
6. Model saved using **pickle (`svc.pkl`)**

---

##   Flask Web App

* Backend: `main.py` loads model + datasets and handles predictions
* Frontend: `index.html` form for user symptom input
* Output: Displays predicted disease, description, precautions, medications, workout & diet

Run locally:

```bash
# Create virtual environment
python -m venv venv
source venv/bin/activate  # (Linux/Mac)
venv\Scripts\activate     # (Windows)

 
# Run Flask app
python main.py
```

Visit: 👉 `http://127.0.0.1:5000/`

---

## 📊 Example Usage

**Input Symptoms:**

```
itching, skin_rash, nodal_skin_eruptions
```

**Predicted Disease:**

```
Fungal Infection
```

**Precautions:**

* Bath twice daily
* Use Dettol or neem in bathing water
* Keep infected area dry
* Wear clean clothes

**Medications:**

* Antifungal Cream
* Fluconazole
* Terbinafine
* Clotrimazole
* Ketoconazole

 
---
 
*   [LinkedIn](https://www.linkedin.com/in/imadkhan-datascience)
 

 
