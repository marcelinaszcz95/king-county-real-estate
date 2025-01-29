
# **King County Housing Price Predictor**  
### *By: Marcelina Szczygiel*  

## **Introduction**  
This project is an in-depth exploration of the **King County Housing Dataset**, it includes:  
- **Exploratory Data Analysis (EDA)** and data cleaning  
- **Feature engineering & selection**  
- **Data visualization**  
- **Data Preprocessing Pipeline**  (in progress)
- **Model selection and evaluation** (in progress)
- **Stacking models for final price prediction** (in progress)

The project is structured into multiple notebooks, each covering different aspects of the analysis and modeling.  

---

## **Project Structure**  

### 📂 **Notebooks & Files**  
#### 🔹 `KC_EDA.ipynb` – Exploratory Data Analysis & Hypothesis Testing  
This notebook contains an **in-depth analysis** of housing data for a specific buyer, based on the following hypotheses:  

#### 📌 **Buyer Profile: Jacob Phillips**  
- **Budget**: Unlimited  
- **Requirements**:  
  - **4+ bathrooms** or **smaller house nearby**  
  - **Large lot** (Tennis court & pool)  
  - **Golf course nearby**  
  - **Historic appeal**  
  - **No waterfront**  



#### 🧪 **Hypothesis Testing**  
1. **Historical Significance & Pricing**  
   - Houses **built before 1940** have **higher prices** than modern homes (**post-2005**).  
   - These homes also have **larger lots** (>15,000 sqft).  

2. **Luxury Amenities in Modern Homes**  
   - Homes with **4+ bathrooms** are **mostly modern** (built post-2005).  
   - They include **luxury features** such as:  
     - **King County Grade**  
     - **Condition Scale**  
     - **View Quality**  
     - **Waterfront access**  

3. **High-Grade Homes & Prime Locations**  
   - Homes with a **King County Grade >10** are in **scenic areas** (View Quality >3).  
   - They are located near **golf courses** and other premium facilities.  

---

## **Next Steps**  

🚀 The next phase of the project will focus on **automating and optimizing** the data processing and modeling pipeline. The key components include:  

### **1️⃣ Data Preprocessing Pipeline**  
🔹 **Loading & Cleaning Data**  
- Handle missing values (imputation or removal).  
- Correct data types (e.g., categorical encoding, datetime conversion).  
- Remove duplicates and outliers.  

🔹 **Feature Engineering & Selection**  
- Create meaningful features (e.g., house age categories, lot size bins).  
- Normalize/scale numerical features.  
- Encode categorical features (e.g., one-hot encoding, label encoding).  
- Perform feature selection (filter methods, embedded methods like Lasso).  

### **2️⃣ Model Training Pipeline**  
🔹 **Train/Test Split & Cross-Validation**  
- Implement stratified train-test splitting.  
- Apply **k-fold cross-validation** for robust evaluation.  

🔹 **Model Selection & Optimization**  
- Compare multiple models:  
  - **Linear Regression, Random Forest, XGBoost, Gradient Boosting**  
- Tune hyperparameters using **GridSearchCV/Optuna**.  

🔹 **Stacking & Ensemble Learning**  
- Blend multiple models to improve accuracy and reduce variance.  

### **3️⃣ Deployment Pipeline (Future Scope)**  
🔹 **Automate Model Predictions**  
- Convert the trained model into a **deployable API** (e.g., Flask, FastAPI).  
- Create a user interface for real-time predictions.  


---



## **Skills Presented**  

✅ **Data Cleaning**  
- Handling missing values, outlier detection, and data type conversion.  

✅ **Exploratory Data Analysis (EDA)**  
- Statistical analysis and hypothesis testing.  
- Identifying trends, correlations, and patterns in housing prices.  

✅ **Data Visualization**  
- Using **Matplotlib** and **Seaborn** for visual insights.  
- Creating plots like histograms, scatter plots, and heatmaps to explore relationships.  

✅ **Feature Selection and Engineering**  
- Creating new features (e.g., house age categories, lot size bins).  
- Encoding categorical variables and selecting important predictors.  

🚀 **In Progress:**  
🛠️ **Creating an automatic pipeline for data preprocessing**  
- Automating feature engineering, transformation, and cleaning.  

🛠️ **Model Selection and Tuning**  
- Evaluating multiple models and optimizing hyperparameters with **GridSearchCV/Optuna**.  

🛠️ **Model Stacking**  
- Implementing ensemble learning techniques to improve accuracy.  





## Requirements

- pyenv
- python==3.11.3

## Setup

One of the first steps when starting any data science project is to create a virtual environment. For this project you have to create this environment from scratch yourself. However, you should be already familiar with the commands you will need to do so. The general workflow consists of... 

* setting the python version locally to 3.11.3
* creating a virtual environment using the `venv` module
* activating your newly created environment 
* upgrading `pip` (This step is not absolutely necessary, but will save you trouble when installing some packages.)
* installing the required packages via `pip`

At the end, you want to make sure that people who are interested in your project can create an identical environment on their own computer in order to be able to run your code without running into errors. Therefore you can create a `requirements file` and add it to your repository. You can create such a file by running the following command: 

```bash
pip freeze > requirements.txt
```

*Note: In rare case such a requirements file created with `pip freeze` might not ensure that another (especially M1 chip) user can install and execute it properly. This can happen if libraries need to be compiled (e.g. SciPy). Then it also depends on environment variables and the actual system libraries.*


## Set up your Environment
This repo contains a requirements.txt file with a list of all the packages and dependencies you will need.

Before you can start with plotly in Jupyter Lab you have to install node.js (if you haven't done it before).
- Check **Node version**  by run the following commands:
    ```sh
    node -v
    ```
    If you haven't installed it yet, begin at `step_1`. Otherwise, proceed to `step_2`.


### **`macOS`** type the following commands : 


- `Step_1:` Update Homebrew and install Node by following commands:
    ```sh
    brew update
    brew install node
    ```

- `Step_2:` Install the virtual environment and the required packages by following commands:

    ```BASH
    pyenv local 3.11.3
    python -m venv .venv
    source .venv/bin/activate
    pip install --upgrade pip
    pip install -r requirements.txt
    ```
### **`WindowsOS`** type the following commands :


- `Step_1:` Update Chocolatey and install Node by following commands:
    ```sh
    choco upgrade chocolatey
    choco install nodejs
    ```

- `Step_2:` Install the virtual environment and the required packages by following commands.

   For `PowerShell` CLI :

    ```PowerShell
    pyenv local 3.11.3
    python -m venv .venv
    .venv\Scripts\Activate.ps1
    pip install --upgrade pip
    pip install -r requirements.txt
    ```

    For `Git-Bash` CLI :
  
    ```BASH
    pyenv local 3.11.3
    python -m venv .venv
    source .venv/Scripts/activate
    pip install --upgrade pip
    pip install -r requirements.txt
    ```
 

 **`Note:`**
    If you encounter an error when trying to run `pip install --upgrade pip`, try using the following command:

   ```Bash
   python.exe -m pip install --upgrade pip
   ```
