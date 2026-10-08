# 📈 Sales Prediction Using Python

A machine learning project that predicts product **sales** from **advertising spend** across three channels — **TV**, **Radio**, and **Newspaper** — using and comparing **Linear Regression** and **Random Forest Regression** models.

## 🎯 Project Overview

Advertising budgets are one of the biggest levers businesses can pull to drive sales — but not all channels are equally effective. This project uses the classic **Advertising dataset** (200 records) to:

- Explore how each advertising channel relates to sales
- Train two regression models to predict sales from advertising spend
- Compare model performance and interpret which channels matter most
- Predict sales for a brand-new advertising budget

## 🗂️ Dataset

**File:** [`Advertising.csv`](./Advertising.csv)

| Column      | Description                                   |
|-------------|------------------------------------------------|
| `TV`        | Advertising budget spent on TV (in $ thousands)        |
| `Radio`     | Advertising budget spent on Radio (in $ thousands)      |
| `Newspaper` | Advertising budget spent on Newspaper (in $ thousands)  |
| `Sales`     | Product sales (in thousands of units)          |

200 rows, no missing values, no duplicates.

## 🧠 Approach

1. **Data Cleaning** — drop the redundant index column, check for nulls/duplicates.
2. **Exploratory Data Analysis** — scatter plots, distributions, boxplots, and a correlation heatmap to understand each channel's relationship with sales.
3. **Modeling** — split the data 80/20 and train:
   - **Linear Regression** — a simple, interpretable baseline
   - **Random Forest Regressor** — a more flexible ensemble model
4. **Evaluation** — compare both models using MAE, MSE, RMSE, and R².
5. **Interpretation** — inspect Linear Regression coefficients and Random Forest feature importances to see which channel drives sales the most.
6. **Prediction** — use the trained models to predict sales for a new advertising budget.

## 📊 Results

| Model              | MAE   | RMSE  | R² Score |
|--------------------|-------|-------|----------|
| Linear Regression   | ~1.46 | ~1.78 | ~0.90    |
| Random Forest       | ~0.62 | ~0.77 | ~0.98    |

**Random Forest outperforms Linear Regression** on every metric, capturing non-linear relationships in the data that the linear model misses. **TV advertising** has the strongest influence on sales, followed by **Radio**, while **Newspaper** contributes the least.

*(Exact numbers may vary slightly depending on your environment/package versions.)*

## 🛠️ Tech Stack

- Python 3
- pandas, numpy — data handling
- matplotlib, seaborn, plotly — visualization
- scikit-learn — modeling & evaluation

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Run the notebook
```bash
jupyter notebook Sales_Prediction_Using_Python.ipynb
```

## 📁 Project Structure
```
.
├── Advertising.csv                    # Dataset
├── Sales_Prediction_Using_Python.ipynb  # Main notebook: EDA, modeling, evaluation
├── requirements.txt                   # Python dependencies
└── README.md                          # Project documentation
```

## 🔮 Example Prediction

For a budget of **$150K on TV, $25K on Radio, and $20K on Newspaper**, the models predict sales of roughly **14.5–15.2 thousand units**.

## 📌 Notes

- The dataset is a well-known toy dataset commonly used for regression practice (originally from *An Introduction to Statistical Learning*).
- This project is for educational/portfolio purposes.

## 📄 License

This project is open source and available under the [MIT License](https://opensource.org/licenses/MIT).
