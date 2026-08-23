# 💵 Banknote Authentication using Decision Tree

## 📌 Project Overview

This project uses **Machine Learning** to classify a banknote as **Real or Fake** using a **Decision Tree Classifier**.

Two Decision Tree criteria were compared:

* Gini
* Entropy

The models were trained using the same train-test split with `random_state=42`.

The results were:

| Model                   |  Accuracy |
| ----------------------- | --------: |
| Decision Tree - Gini    | **98.1%** |
| Decision Tree - Entropy | **98.5%** |

Since **Entropy achieved the higher accuracy**, it was selected as the final model.

The trained model is saved using **Pickle** and deployed using **Streamlit**.

---

## 🎯 Project Objective

The objective of this project is to:

1. Load the banknote dataset.
2. Perform basic data preparation.
3. Separate features and target.
4. Split the data into training and testing sets.
5. Train a Decision Tree using Gini.
6. Train a Decision Tree using Entropy.
7. Compare the model accuracies.
8. Select the best-performing model.
9. Save the selected model using Pickle.
10. Create a Streamlit application.
11. Predict whether a banknote is **Real or Fake**.
12. Deploy the application.

---

## 📊 Dataset

The dataset contains information about banknotes.

### Dataset Features

| Feature  | Description                    |
| -------- | ------------------------------ |
| Variance | Variance of the banknote image |
| Skewness | Skewness of the banknote image |
| Curtosis | Curtosis of the banknote image |
| Entropy  | Entropy of the banknote image  |
| Class    | Target variable                |

The input features used by the model are:

```text
Variance
Skewness
Curtosis
Entropy
```

The target column is:

```text
Class
```

For the standard Banknote Authentication dataset:

```text
Class 0 → Real / Genuine
Class 1 → Fake / Forged
```

---

## 🤖 Machine Learning Algorithm

The algorithm used is:

**Decision Tree Classifier**

Two criteria were compared.

### Gini

```python
DecisionTreeClassifier(
    criterion="gini",
    random_state=42
)
```

### Entropy

```python
DecisionTreeClassifier(
    criterion="entropy",
    random_state=42
)
```

The same train-test split was used for both models:

```python
X_train, X_test, y_train, y_test = train_test_split(
    X,
    y,
    test_size=0.20,
    random_state=42
)
```

Using the same `random_state=42` makes the comparison fair and repeatable.

---

## 📈 Model Comparison

The model performance was:

```text
Gini Accuracy    = 98.1%
Entropy Accuracy = 98.5%
```

### 🏆 Selected Model

The **Entropy Decision Tree** was selected because it achieved the higher test accuracy.

```python
DecisionTreeClassifier(
    criterion="entropy",
    random_state=42
)
```

### Final Accuracy

**98.5%**

---

## 💾 Model Saving

The trained model was saved using Python's `pickle` module.

```python
import pickle

with open("decision_tree_entropy.pkl", "wb") as file:
    pickle.dump(dt_entropy, file)
```

The saved model is:

```text
decision_tree_entropy.pkl
```

This file is loaded by the Streamlit application.

---

# 🌐 Streamlit Application

The project includes a Streamlit web application.

The user enters four values:

```text
Variance
Skewness
Curtosis
Entropy
```

The application sends these values to the trained Decision Tree model.

The model then predicts:

```text
Real Banknote
```

or

```text
Fake Banknote
```

The application also displays prediction probabilities and a **Feature Importance** graph.

---

## 📁 Project Structure

```text
Banknote_Authentication/
│
├── app.py
├── train_model.py
├── decision_tree_entropy.pkl
├── requirements.txt
├── README.md
├── .gitignore
└── cff2f578-527b-4fef-89bd-55d79a8fae8e.csv
```

### File Description

#### `app.py`

Contains the Streamlit application and prediction interface.

#### `train_model.py`

Contains the code for:

* Loading the dataset
* Splitting the data
* Training the Decision Tree
* Calculating accuracy
* Saving the model

#### `decision_tree_entropy.pkl`

Contains the trained Entropy Decision Tree model.

#### `requirements.txt`

Contains the Python packages required to run the project.

#### `README.md`

Contains project documentation.

#### `.gitignore`

Prevents unnecessary files such as the virtual environment from being uploaded to GitHub.

---

# 🐍 Virtual Environment

A Python virtual environment is used to keep the project's dependencies separate from other Python projects.

## Create Virtual Environment

Open the terminal inside the project folder:

```bash
python -m venv venv
```

This creates:

```text
venv/
```

---

## Activate Virtual Environment

### Windows Command Prompt

```cmd
venv\Scripts\activate.bat
```

### Windows PowerShell

```powershell
venv\Scripts\Activate.ps1
```

After activation, you should see:

```text
(venv)
```

at the beginning of the terminal.

---

# 📦 Install Required Libraries

After activating the virtual environment, install the required libraries:

```bash
pip install streamlit pandas numpy scikit-learn matplotlib
```

---

# 📄 requirements.txt

The project uses `requirements.txt` to store the installed dependencies.

It can be created using:

```bash
pip freeze > requirements.txt
```

To view the file:

### Windows CMD

```cmd
type requirements.txt
```

The file contains the packages and their versions required by the project.

---

# ▶️ Run the Project Locally

## Step 1 — Activate the virtual environment

```cmd
venv\Scripts\activate.bat
```

## Step 2 — Run Streamlit

```bash
streamlit run app.py
```

The application will start at:

```text
http://localhost:8501
```

Open this address in your browser.

---

# 🖥️ Application Workflow

```text
User enters banknote values
          ↓
Variance
Skewness
Curtosis
Entropy
          ↓
Entropy Decision Tree
          ↓
Prediction
          ↓
Real / Fake
```

---

# 📊 Feature Importance

The application displays a feature importance graph using:

```python
model.feature_importances_
```

The graph helps show the contribution of:

* Variance
* Skewness
* Curtosis
* Entropy

to the Decision Tree model.

---

# 🚀 Deployment

This project can be deployed using **Streamlit Community Cloud**.

## Step 1 — Upload the project to GitHub

Make sure the repository contains:

```text
app.py
train_model.py
decision_tree_entropy.pkl
requirements.txt
README.md
.gitignore
```

---

## Step 2 — Do NOT upload the virtual environment

The `venv` folder should **not** be uploaded to GitHub.

Add the following to `.gitignore`:

```text
venv/
__pycache__/
*.pyc
```

---

## Step 3 — Push the project to GitHub

Run:

```bash
git add .
```

Then:

```bash
git commit -m "Added Banknote Authentication ML project"
```

Then:

```bash
git push
```

---

## Step 4 — Deploy with Streamlit

Go to Streamlit Community Cloud:

https://share.streamlit.io/

Sign in using GitHub.

Select the GitHub repository containing this project.

Select:

```text
Branch: main
Main file: app.py
```

Then click **Deploy**.

Streamlit will install the dependencies from:

```text
requirements.txt
```

and run:

```text
app.py
```

---

# 🔐 Important Deployment Files

The most important files for deployment are:

```text
app.py
decision_tree_entropy.pkl
requirements.txt
```

The `requirements.txt` file tells Streamlit which Python packages to install.

The `.pkl` file contains the trained machine learning model.

The `app.py` file contains the Streamlit application.

---

# 🧪 Example Prediction

Example input:

```text
Variance = 3.62
Skewness = 8.66
Curtosis = -2.80
Entropy = -0.44
```

The values are converted into:

```python
[[3.62, 8.66, -2.80, -0.44]]
```

The model then predicts the class.

Depending on the model prediction:

```text
Class 0 → Real
```

or:

```text
Class 1 → Fake
```

---

# 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Streamlit
* Pickle
* Git
* GitHub
* Virtual Environment

---

# 📚 Libraries Used

```text
pandas
numpy
scikit-learn
matplotlib
streamlit
```

The exact installed versions are maintained in:

```text
requirements.txt
```

---

# 📌 Important Notes

* The model uses **Entropy** as the Decision Tree criterion.
* The final test accuracy obtained was **98.5%**.
* The model expects four features in this exact order:

```text
Variance
Skewness
Curtosis
Entropy
```

* `Class` is the target and should not be entered as an input.
* The virtual environment (`venv`) should not be uploaded to GitHub.
* The pickle model must be available to `app.py` when deploying the application.

---

# 🏆 Final Result

| Item               | Result                      |
| ------------------ | --------------------------- |
| Algorithm          | Decision Tree               |
| Gini Accuracy      | **98.1%**                   |
| Entropy Accuracy   | **98.5%**                   |
| Selected Criterion | **Entropy**                 |
| Final Model        | `decision_tree_entropy.pkl` |
| Interface          | Streamlit                   |
| Deployment         | Streamlit Community Cloud   |

---

# 👩‍💻 Author

**Shivani**

## Banknote Authentication Machine Learning Project

Built using **Python, Decision Tree, Pickle, Virtual Environment, and Streamlit**.
