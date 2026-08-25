# 📊 Employee Income Clustering using K-Means

A Machine Learning project that uses **K-Means Clustering** to group employees based on their **Age** and **Income**. The trained clustering model is integrated into an interactive **Streamlit web application** for data visualization and cluster prediction.

---

## 🚀 Project Overview

This project demonstrates an **Unsupervised Machine Learning** approach using the **K-Means Clustering algorithm**.

The application allows users to:

* Upload an employee dataset in CSV format
* Preview the uploaded data
* Group employees into clusters based on **Age** and **Income**
* View cluster counts
* Analyze average Age and Income for each cluster
* Visualize clusters using a scatter plot
* View K-Means model inertia
* Enter new Age and Income values
* Predict the cluster of a new employee

The Streamlit application loads the trained K-Means model from `kmeans.pkl`.

---

## 🎯 Project Objective

The main objective of this project is to apply **K-Means Clustering** to employee data and identify groups of employees with similar characteristics based on:

* **Age**
* **Income**

The project also demonstrates how an unsupervised Machine Learning model can be integrated into a user-friendly Streamlit application.

---

## 🧠 Machine Learning Algorithm

### K-Means Clustering

K-Means is an **unsupervised Machine Learning algorithm** used to divide data points into a predefined number of clusters.

In this project, the trained K-Means model contains **5 clusters**.

The model uses the following features:

```text
Age
Income
```

Before clustering, the application applies **MinMaxScaler** to the input features.

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

The clustering model uses only:

```text
Age
Income
```

The `Name` column is not used for clustering.

---

## 🔄 Machine Learning Workflow

```text
Employee Dataset
       ↓
Select Age & Income
       ↓
Data Scaling
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

### 1. CSV Dataset Upload

Users can upload a CSV file containing `Age` and `Income` columns.

The application displays the first few rows of the uploaded dataset.

### 2. Cluster Count

The application displays the number of employees belonging to each cluster.

### 3. Summary Statistics

The application calculates the average Age and Income for each cluster.

### 4. Cluster Visualization

A scatter plot is generated to visualize the employee clusters based on Age and Income.

The cluster centers are also displayed on the graph.

### 5. Model Inertia

The application displays the K-Means **inertia value**, which represents the within-cluster sum of squared distances.

### 6. New Employee Prediction

Users can enter:

```text
Age
Income
```

and click **Predict Cluster** to determine which cluster the new employee belongs to.

---

## 📊 Model Information

| Parameter          | Value              |
| ------------------ | ------------------ |
| Algorithm          | K-Means Clustering |
| Number of Clusters | 5                  |
| Features           | Age, Income        |
| Scaling            | MinMaxScaler       |
| Model File         | `kmeans.pkl`       |
| Application        | Streamlit          |

---

## 📁 Project Structure

```text
Employee-Income-KMeans-Clustering/
│
├── app.py
├── kmeans.pkl
├── scaler.pkl
├── Employee_income_1.csv
├── requirements.txt
├── README.md
└── .gitignore
```

### File Description

| File                    | Description                                         |
| ----------------------- | --------------------------------------------------- |
| `app.py`                | Streamlit application for clustering and prediction |
| `kmeans.pkl`            | Trained K-Means clustering model                    |
| `scaler.pkl`            | Saved feature scaling object                        |
| `Employee_income_1.csv` | Employee Age and Income dataset                     |
| `requirements.txt`      | Python dependencies                                 |
| `README.md`             | Project documentation                               |
| `.gitignore`            | Files excluded from GitHub                          |

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
git clone https://github.com/your-username/employee-income-kmeans-clustering.git
```

### Step 2: Navigate to the Project Folder

```bash
cd employee-income-kmeans-clustering
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

```powershell
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

Default local address:

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

The application will display:

* Raw data preview
* Cluster count
* Summary statistics
* Cluster visualization
* Cluster centers
* Model inertia

### Step 4

Enter a new employee's:

```text
Age
Income
```

### Step 5

Click:

```text
Predict Cluster
```

The application will display the predicted cluster.

---

## 📊 Example Input

```text
Age    = 30
Income = 100000
```

The application processes the values and predicts the corresponding K-Means cluster.

---

## 📸 Project Screenshot

Add your Streamlit application screenshot to a folder named:

```text
screenshots/
```

For example:

```text
screenshots/
└── kmeans-app.png
```

Then add this section to the README:

```markdown
## 📸 Project Screenshot

Click the image below to view the full-size screenshot.

[![K-Means Clustering Application](screenshots/kmeans-app.png)](screenshots/kmeans-app.png)
```

This makes the screenshot clickable so visitors can open the full-size image.

---

## 🔍 Key Learning Outcomes

Through this project, I practiced:

* Unsupervised Machine Learning
* K-Means Clustering
* Feature Scaling
* Model Serialization using Pickle
* Data Visualization
* Cluster Analysis
* Streamlit Application Development
* CSV File Upload
* Git and GitHub
* Machine Learning Model Deployment

---

## ⚠️ Important Notes

* The uploaded CSV must contain `Age` and `Income` columns.
* The application uses these two features for clustering.
* The trained K-Means model is loaded from `kmeans.pkl`.
* The virtual environment should not be uploaded to GitHub.
* Keep the model files in the same project directory as `app.py`.
* The Python package versions are maintained in `requirements.txt`.

---

## 🚀 Future Improvements

Possible improvements for this project include:

* Add an Elbow Method visualization
* Add Silhouette Score analysis
* Allow users to select the number of clusters
* Add downloadable clustered data
* Add more employee features
* Improve the Streamlit user interface
* Deploy the application using Streamlit Community Cloud

---

## 👩‍💻 Author

**Shivani Patil**

### Machine Learning & Data Science Project

Built with **Python, K-Means Clustering, Scikit-learn, Pandas, Matplotlib, Seaborn, and Streamlit**.

---

## ⭐ If You Like This Project

If you find this project useful, consider giving the repository a ⭐ on GitHub.
