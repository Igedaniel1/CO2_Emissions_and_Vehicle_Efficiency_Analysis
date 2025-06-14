# 🚗 CO₂ Emissions & Vehicle Efficiency Analysis

This project analyzes a real-world dataset of vehicle specifications, fuel consumption, and CO₂ emissions to support environmental policy, guide consumer choices, and uncover insights on fuel efficiency and emission patterns across different vehicle types and engine sizes.

---

## 📊 Dataset Overview

The dataset (`CO2_Emission.csv`) includes the following features:

| Column                          | Description |
|---------------------------------|-------------|
| `Model_year`                    | Year the vehicle model was released |
| `Make`                          | Manufacturer of the vehicle |
| `Model`                         | Vehicle model name |
| `Vehicle_Class`                | Vehicle type (e.g., SUV, Compact) |
| `Engine_size` (L)              | Engine displacement in liters |
| `Cylinders`                    | Number of engine cylinders |
| `Transmission`                | Transmission code (e.g., AS8, M6) |
| `Fuel_Consumption_in_City`    | Fuel usage in city driving (L/100km) |
| `Fuel_Consumption_in_City_Hwy`| Fuel usage on highways (L/100km) |
| `Fuel_Consumption_comb`       | Combined average fuel consumption |
| `CO2_Emissions` (g/km)        | CO₂ emitted per kilometer |
| `Smog_Level`                   | Air pollution level from vehicle emissions |

---

## 🧠 Project Goals

- **Environmental policy**: Identify high-emission vehicle types and trends to support regulation.
- **Consumer support**: Highlight eco-friendlier vehicles based on emissions and efficiency.
- **Engineering insights**: Understand how engine size, transmission, and vehicle class impact emissions.

---

## 🔍 Key Questions Answered

### Emissions & Environmental Impact
- What is the average CO₂ emission across all vehicle classes?
- Which vehicle classes emit the most and least CO₂ on average?
- How have emissions changed by `Model_year`?
- What is the distribution of smog levels across vehicle classes?
- How does `Smog_Level` correlate with fuel consumption and emissions?

### Vehicle Efficiency & Engine Performance
- Which vehicles have the lowest CO₂ emissions and highest fuel efficiency?
- Do automatic or manual transmissions have better fuel economy?
- Which makes/models offer the best balance of engine performance and low emissions?
- Which vehicles fall below the eco-friendly threshold of 150 g/km?

### Technical & Classification Insights
- How does fuel consumption (city vs highway) vary with engine size?
- Do smaller engines (<2.0L) consistently produce lower emissions?
- Which vehicle class has the highest average highway fuel efficiency?
- Can we classify vehicles as “Eco-Friendly” vs “High Emission”?

---

## 🤖 Machine Learning: CO₂ Emission Classification

To automate eco-friendliness labeling, a **Classifier** was built, using a pie chart to visually display eco friendly and highu emission vehicl classes.

### 🏷️ Labeling Criteria
- **Eco-Friendly**: CO₂ emissions < 150 g/km
- **High Emission**: CO₂ emissions ≥ 150 g/km

### 🛠 Model Pipeline- To build a regression model to predict CO2 Emissions based on different vehicle features.
1. **Feature Engineering**: Transmission type derived from code prefixes (e.g., A8 → Automatic).
2. **Preprocessing**: One-hot encoding for categorical features.
3. **Train-Test Split**: 70/30
4. **Model**: Random Forest Regressor (`sklearn`)
5. **Evaluation Metrics**:
   - **Accuracy**: `0.96`
   - High precision and recall across both classes

### 🧠 Key Features Used
- `Engine_size`
- `Fuel_Consumption_comb`
- `Vehicle_Class`
- `Transmission_Type`
- `CO2_Emissions`

---

## 📈 Visualizations

Visuals generated using `matplotlib` and `seaborn`:
- Line chart: CO₂ emission trends over time
- Bar chart: Fuel consumption by transmission type
- Boxplot: Emissions by vehicle class
- Scatter plot: Engine size vs fuel consumption
- Histogram: Smog level distribution

Data summaries are export-ready for interactive dashboards in **Power BI** or **Tableau**.

---

## 🗃️ Project Files

| File | Description |
|------|-------------|
| `co2_Emissions_Analysis.ipynb` | Full Jupyter notebook with EDA, feature engineering, modeling, and visuals |
| `README.md`                    | Project overview |
| `eco_friendly_buy.ipynb`       | Vehicles that are friendly to eco system |
| `vehicle_performance.ipynb`    | Vehicle performance |
| `co2_predictive_model.ipynb`   | The model Prediction for co2 emissions |
| `CO2_emission.csv`             | Raw Dataset |

---

## 📦 Tools & Libraries

- Python (Pandas, NumPy)
- Data Viz: Seaborn, Matplotlib
- Machine Learning: Scikit-learn
- Jupyter Notebook
- Tableau / Power BI (for dashboard integration)

---

## 💡 How to Use

1. Clone the repo:
   ```bash
   git clone https://github.com/your-username/co2-emissions-analysis.git
   cd co2-emissions-analysis
