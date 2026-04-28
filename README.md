# ⚡ Electric Vehicles Data Analysis

An end-to-end Exploratory Data Analysis (EDA) project on Electric Vehicles using Python. The project covers data cleaning, univariate, bivariate, and multivariate analysis with rich visualizations to uncover insights about EV pricing, battery performance, range, and manufacturer trends.

---

## 📁 Dataset

**File:** `project_electric vehicles.csv`

**Key Columns:**

| Column | Type | Description |
|---|---|---|
| `company` | Categorical | EV Manufacturer |
| `models` | Categorical | Car Model Name |
| `prices` | Continuous | Price in Euros (€) |
| `battery` | Continuous | Battery Capacity (kWh) |
| `range` | Discrete | Driving Range (km) |
| `fastcharge` | Discrete | Fast Charging Speed (kW) |
| `efficiency` | Discrete | Energy Efficiency (Wh/km) |
| `weight` | Continuous | Vehicle Weight (kg) |

---

## 🔧 Tech Stack

| Tool | Purpose |
|---|---|
| Python | Core programming language |
| Pandas | Data manipulation & cleaning |
| NumPy | Numerical operations |
| Matplotlib | Plotting & visualizations |
| Seaborn | Statistical visualizations |
| Jupyter Notebook | Interactive development environment |

---

## 📊 Project Workflow

### 1. 📥 Data Loading & Inspection
- Loaded dataset using Pandas
- Checked shape, data types, and column names
- Identified total missing values per column

### 2. 🧹 Data Cleaning
- Dropped unnecessary columns (`Unnamed: 0`)
- Standardized column names (lowercase, underscores)
- Removed unit symbols (`€`, `km`, `kWh`, `kW`, `Wh/km`, `kg`)
- Converted all feature columns to numeric types
- Filled missing values with **median** for numeric columns and **mode** for categorical columns
- Removed duplicate rows
- Filtered out invalid/negative values
- Detected and treated **outliers using the IQR method**

### 3. 📈 Univariate Analysis

**Continuous Variables** (`prices`, `battery`, `range`, `fastcharge`, `efficiency`, `weight`):
- Statistical summary: Mean, Median, Mode, Min, Max, Std Dev, Variance, Skewness
- Histogram & Distribution Plot
- Box Plot (outlier detection)
- Violin Plot
- KDE Plot

**Categorical Variables** (`company`, `models`):
- Frequency Distribution & Percentage Distribution
- Count Plot (Top 20)
- Bar Plot
- Pie Chart (Company Distribution)

### 4. 🔗 Bivariate & Multivariate Analysis

- **Categorical vs Continuous:** Average price by company (Top 10 & 15), Pivot table (price & battery by company)
- **Continuous vs Continuous:** Correlation matrix, Heatmap (coolwarm & viridis), Scatter plot (Battery vs Range)
- **Categorical vs Categorical:** Crosstab (Company vs Models), Heatmap of crosstab (Top 20 cars by range)

---

## 📌 Key Insights

- EV prices are **right-skewed**, with a few premium brands driving up the average
- **Battery capacity** shows a strong positive correlation with **driving range**
- **Efficiency (Wh/km)** varies significantly across manufacturers
- A few companies dominate the EV market in terms of model count
- Top-range EVs tend to have **larger batteries** but not always higher prices

---

## 📂 Project Structure

```
ev-data-analysis/
│
├── ev_project_.ipynb              # Main Jupyter Notebook
├── project_electric_vehicles.csv  # Dataset
└── README.md                      # Project documentation
```

---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/ev-data-analysis.git
   cd ev-data-analysis
   ```

2. Install required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn
   ```

3. Launch Jupyter Notebook:
   ```bash
   jupyter notebook ev_project_.ipynb
   ```

---

## 📸 Screenshots
<img width="771" height="528" alt="image" src="https://github.com/user-attachments/assets/90d4a77d-438d-4bb0-89ee-2ca4fd639e69" />
<img width="1237" height="579" alt="image" src="https://github.com/user-attachments/assets/9c1ea3d3-3007-4f15-9eb1-77f0408fad97" />
<img width="1234" height="575" alt="image" src="https://github.com/user-attachments/assets/c0f42245-c88d-4b28-9dcf-5975e8c68c4c" />
<img width="815" height="818" alt="image" src="https://github.com/user-attachments/assets/4460d853-f597-4ff1-b817-4ebde8f34257" />
<img width="1097" height="682" alt="image" src="https://github.com/user-attachments/assets/a1aa534b-0834-49ab-898b-8f85ddcb9554" />
<img width="797" height="656" alt="image" src="https://github.com/user-attachments/assets/0cd35b3f-5f06-4268-a50c-36a14c5391df" />







---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
