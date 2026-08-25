# 📊 Employee Income Clustering using K-Means

A Machine Learning project that uses **K-Means Clustering** to group employees based on their **Age** and **Income**. The trained model is integrated with an interactive **Streamlit web application** for cluster analysis, visualization, and prediction.

---

## 🚀 Project Overview

This project demonstrates an **Unsupervised Machine Learning** approach using the **K-Means Clustering algorithm**.

The Streamlit application allows users to:

* Upload an employee dataset in CSV format
* Preview the uploaded dataset
* Group employees into different clusters
* Analyze cluster-wise employee information
* View cluster counts
* Calculate average Age and Income for each cluster
* Visualize employee clusters using a scatter plot
* View K-Means inertia
* Enter Age and Income for a new employee
* Predict the cluster of a new employee

The trained K-Means model is stored in `kmeans.pkl`, while the feature scaler is stored in `scaler.pkl`.

---

## 🎯 Project Objective

The main objective of this project is to identify groups of employees with similar characteristics using:

* **Age**
* **Income**

The project demonstrates how an unsupervised Machine Learning model can be trained, saved, and integrated into a user-friendly Streamlit application.

---

## 🧠 Machine Learning Algorithm

### K-Means Clustering

**K-Means Clustering** is an unsupervised Machine Learning algorithm that divides data points into a predefined number of clusters.

In this project:

* **Algorithm:** K-Means Clustering
* **Number of Clusters:** 5
* **Features:** Age and Income
* **Scaling:** MinMaxScaler

Before applying K-Means, the Age and Income features are scaled using `MinMaxScaler`.

---

## 📂 Dataset

The project uses an employee income dataset containing the following columns:

| Column   | Description     |
| -------- | --------------- |
| `Name`   | Employee name   |
| `Age`    | Employee age    |
| `Income` | Employee income |

### Dataset Example

| Name   | Age | Income |
| ------ | --: | -----: |
| Amit   |  27 |  70000 |
| Akash  |  29 |  90000 |
| Shriya |  29 |  61000 |
| Anita  |  28 |  62000 |
| Sudhir |  42 | 155000 |

The `Name` column is used for identification only. The clustering model uses:

```text
Age
Income
```

---

## 🔄 Machine Learning Workflow

```text
Employee Dataset
       ↓
Select Age & Income
       ↓
Feature Scaling
       ↓
K-Means Clustering
       ↓
Assign Cluster Labels
       ↓
Analyze Clusters
       ↓
Visualize Clusters
       ↓
Predict Cluster for New Employee
```

---

## 📈 Application Features

### 1. 📁 CSV Dataset Upload

Users can upload a CSV file containing `Age` and `Income` columns.

The application displays a preview of the uploaded dataset.

### 2. 📊 Cluster Count

The application displays the number of employees belonging to each cluster.

### 3. 📋 Cluster Summary

The application calculates and displays average:

* Age
* Income

for each cluster.

### 4. 📈 Cluster Visualization

A scatter plot is generated using:

* X-axis → Age
* Y-axis → Income

The visualization helps users understand how employees are grouped.

### 5. 📐 Model Inertia

The application displays the **K-Means inertia value**, which represents the within-cluster sum of squared distances.

### 6. 🔮 New Employee Prediction

Users can enter:

```text
Age
Income
```

and click **Predict Cluster** to determine the cluster of a new employee.

---

## 📊 Model Information

| Parameter          | Value              |
| ------------------ | ------------------ |
| Algorithm          | K-Means Clustering |
| Number of Clusters | 5                  |
| Features           | Age, Income        |
| Scaling            | MinMaxScaler       |
| Model File         | `kmeans.pkl`       |
| Scaler File        | `scaler.pkl`       |
| Application        | Streamlit          |

---

## 📁 Project Structure

```text
Banknote-Authentication-ML/
│
├── Screenshot/
│   ├── app.bn.png.png
│   ├── app.bnt.png.png  
│
├── app.py
├── kmeans.pkl
├── scaler.pkl
├── Employee_income.csv
├── requirements.txt
├── README.md
└── .gitignore
```

### File Description

| File                  | Description                     |
| --------------------- | ------------------------------- |
| `app.py`              | Streamlit application           |
| `kmeans.pkl`          | Trained K-Means model           |
| `scaler.pkl`          | Saved MinMaxScaler              |
| `Employee_income.csv` | Employee Age and Income dataset |
| `requirements.txt`    | Python dependencies             |
| `README.md`           | Project documentation           |
| `.gitignore`          | Files excluded from Git         |
| `Screenshot/`         | Application screenshots         |

---

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Scikit-learn**
* **Matplotlib**
* **Seaborn**
* **Streamlit**
* **Pickle**
* **Git**
* **GitHub**

---

## 📦 Installation

### Step 1: Clone the Repository

```bash
git clone https://github.com/shivani14012004/Banknote-Authentication-ML.git
```

### Step 2: Navigate to the Project Folder

```bash
cd Banknote-Authentication-ML
```

### Step 3: Create a Virtual Environment

```bash
python -m venv venv
```

### Step 4: Activate the Virtual Environment

#### Windows

```bash
venv\Scripts\activate
```

#### Windows PowerShell

```bash
venv\Scripts\Activate.ps1
```

### Step 5: Install Dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Run the Application

Start the Streamlit application using:

```bash
streamlit run app.py
```

The application will open in your browser.

Default local URL:

```text
http://localhost:8501
```

---

## 🖥️ How to Use the Application

### Step 1

Run the Streamlit application.

### Step 2

Upload a CSV file containing:

```text
Age
Income
```

### Step 3

The application displays:

* Dataset preview
* Cluster counts
* Cluster summary
* Cluster visualization
* Cluster centers
* Model inertia

### Step 4

Enter the Age and Income of a new employee.

### Step 5

Click:

```text
Predict Cluster
```

The application will display the predicted cluster.

---

## 📝 Example Input

```text
Age = 30
Income = 100000
```

The application processes these values and predicts the corresponding K-Means cluster.

---

## 📸 Project Screenshots

### Streamlit Application

Click the screenshot to open the **full-size image**.

[![Employee Income K-Means Application](https://github.com/shivani14012004/Banknote-Authentication-ML/blob/main/Screenshot/app.bnt.png.png?raw=true)](https://github.com/shivani14012004/Banknote-Authentication-ML/blob/main/Screenshot/app.bnt.png.png)

### Application Output

[![Employee Income K-Means Output](https://github.com/shivani14012004/Banknote-Authentication-ML/blob/main/Screenshot/app.bn.png.png?raw=true)](https://github.com/shivani14012004/Banknote-Authentication-ML/blob/main/Screenshot/app.bn.png.png)

> **Note:** The screenshots are stored inside the `Screenshot` folder of this repository.

---

## 🔍 Key Learning Outcomes

Through this project, I practiced:

* Unsupervised Machine Learning
* K-Means Clustering
* Feature Scaling
* Model Serialization using Pickle
* Cluster Analysis
* Data Visualization
* Streamlit Application Development
* CSV File Upload
* Machine Learning Model Integration
* Git and GitHub

---

## ⚠️ Important Notes

* The uploaded CSV must contain `Age` and `Income` columns.
* The K-Means model uses Age and Income for clustering.
* The trained model is loaded from `kmeans.pkl`.
* The scaler is loaded from `scaler.pkl`.
* Keep `kmeans.pkl` and `scaler.pkl` in the same project directory as `app.py`.
* Do not upload the virtual environment to GitHub.
* Required Python packages are listed in `requirements.txt`.

---

## 🚀 Future Improvements

Possible improvements include:

* Add Elbow Method visualization
* Add Silhouette Score analysis
* Allow users to select the number of clusters
* Add downloadable clustered data
* Add additional employee features
* Improve the Streamlit user interface
* Add interactive Plotly visualizations
* Deploy the application using Streamlit Community Cloud

---

## 👩‍💻 Author

**Shivani Patil**

Machine Learning & Data Science Enthusiast

### Skills Demonstrated

**Python | Machine Learning | Scikit-learn | Pandas | NumPy | Streamlit | Data Visualization | GitHub**

---

## ⭐ Support

If you find this project useful, consider giving the repository a ⭐ on GitHub.


