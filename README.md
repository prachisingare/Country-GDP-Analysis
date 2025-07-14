# 📊 Country GDP Analysis

A data analysis project using **Pandas**, **NumPy**, **Matplotlib**, and **Seaborn** to explore socio-economic indicators such as **Birth Rate**, **Internet Users**, and **Income Group** across 195 countries. This project is designed to gain insights into development levels and trends in technology access around the globe.

---

## 📁 Dataset Overview

The dataset contains the following columns:

| Column Name     | Description                                      |
|-----------------|--------------------------------------------------|
| `CountryName`   | Name of the country                              |
| `CountryCode`   | ISO 3-letter country code                        |
| `BirthRate`     | Annual number of births per 1,000 people         |
| `InternetUsers` | Percentage of people using the Internet          |
| `IncomeGroup`   | Economic classification by World Bank standards  |

🧾 **Total Records:** 195  
✅ **Missing Values:** None

---

## 🔍 Project Goals

- Understand the relationship between internet access and birth rate.
- Analyze internet usage across different income groups.
- Filter and explore data based on custom conditions (e.g., countries with low internet access and high birth rates).
- Visualize patterns using advanced plotting techniques.

---

## 🛠️ Tools & Technologies

- Python 3.x
- Jupyter Notebook
- **Libraries Used:**
  - `pandas` for data manipulation
  - `seaborn` & `matplotlib` for visualization
  - `numpy` for numerical computations

---

## 📈 Data Analysis Workflow

1. **Data Loading**
   ```python
   df = pd.read_csv("data.csv")
   ```

2. **Initial Exploration**
   - Shape of dataset: `195 rows × 5 columns`
   - Null values: None
   - Basic stats using `df.describe()`

3. **Categorical & Numerical Splits**
   ```python
   df_cat = df[['CountryName', 'CountryCode', 'IncomeGroup']]
   df_num = df[['BirthRate', 'InternetUsers']]
   ```

4. **Filtering Examples**
   - Countries with Internet Users < 2%
   - Countries with Birth Rate > 40
   - High vs. Low income groups

5. **New Feature Engineering**
   ```python
   df['Newcolumn'] = df.BirthRate * df.InternetUsers
   ```

---

## 📊 Visualizations

1. **Distribution of Internet Users**
   ```python
   sns.distplot(df["InternetUsers"])
   ```

2. **Boxplot: Birth Rate by Income Group**
   ```python
   sns.boxplot(data=df, x="IncomeGroup", y="BirthRate")
   ```

3. **Scatterplot with Regression Line**
   ```python
   sns.lmplot(data=df, x="InternetUsers", y="BirthRate", fit_reg=True)
   ```

---

## 📌 Key Insights

- **High-income countries** typically have **low birth rates** and **high internet usage**.
- **Low-income countries** exhibit **higher birth rates** with **limited internet access**.
- A notable cluster of countries exists where both **birth rates are high** and **internet penetration is very low**.

---

## 📚 Future Improvements

- Integrate GDP per capita and literacy rate for deeper analysis.
- Use interactive dashboards (e.g., Plotly, Streamlit).
- Predictive modeling: e.g., predicting income group using ML.

---

## 🧠 Learnings

- Improved skills in data filtering, feature creation, and pandas operations.
- Gained hands-on experience with real-world socio-economic data.
- Learned to visualize and interpret patterns across multiple variables.

