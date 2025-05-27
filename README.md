# Nonlinear-Depreciation
# 📉 Modeling Nonlinear Depreciation with Generalized Additive Models (GAM)

**Author:** Brandy Horne  
**Tags:** GAM, Depreciation Modeling, Pricing Strategy, Nonlinear Modeling, Python, Tableau, CRISP-DM

---

## 🎯 The Business Problem

Traditional linear models often fall short when predicting how product value depreciates over time or usage — especially when that relationship is **nonlinear**, with depreciation accelerating or leveling off at certain thresholds.

This project focused on developing a model to capture the **nonlinear impact of mileage on resale price** for commercial fleet vehicles, with the goal of supporting **data-informed pricing decisions**.

---

## 🔍 Business & Domain Understanding

Pricing teams needed a reliable model that:

- Captured **nonlinear depreciation trends** across mileage bands  
- Provided **intuitive, explainable outputs**  
- Could adjust pricing recommendations for upcoming resale opportunities  

Key insight: The value of commercial assets doesn’t decrease at a constant rate. It often follows **threshold behavior** — steep drops followed by plateaus.

---

## 🧠 Data Understanding

Sourced and evaluated datasets including:

- **Asset specs**: model type, age, drivetrain, warranty status  
- **Usage**: mileage, usage duration, service frequency  
- **Pricing data**: historical resale values, condition at sale  

Exploratory analysis revealed **non-constant slopes** and clear inflection points in mileage vs. price — ideal for GAMs.

---

## 🧹 Data Preparation

- Cleaned and validated pricing data
- Standardized mileage and age features
- Engineered features like:
  - Mileage buckets (e.g., 0–50k, 50–100k…)
  - Age-adjusted residual value
- Detected and excluded outliers using IQR and Z-scores

---

## 🧪 Modeling: Generalized Additive Model (GAM)

I implemented a **GAM** using the `pyGAM` library to allow smooth, flexible fits without losing interpretability.

### Why GAM?
- Captures **nonlinear relationships** with smooth splines
- Retains **explainability** for stakeholder communication
- Handles **interactions** between variables like mileage and model type

**Model Highlights:**
- Smooth function applied to mileage to reveal diminishing return curve
- Factor smooth interaction for vehicle class × mileage
- Cross-validation to prevent overfitting

---

## 📊 Evaluation

- Evaluated using **Adjusted R²**, RMSE, and visual inspection of fit curves
- Compared performance against baseline linear and polynomial models
- Visualized spline functions to highlight key depreciation patterns

**Findings:**
- Depreciation was steepest in the first 100k miles, then leveled
- Certain vehicle types showed nonlinear “elbows” in value curves
- GAM outperformed linear models by 20% in RMSE and had superior interpretability

---

## 📈 Deployment

- Model outputs integrated into pricing dashboards (Tableau)
- Enabled pricing team to visualize predicted price across mileage bands
- Used quarterly to guide buyback and trade-in pricing decisions

---

## ✅ Results

- Improved pricing confidence through model-backed benchmarks
- Enhanced communication of value-loss patterns to non-technical stakeholders
- Influenced new policy around asset lifecycle value projection

---

## 🛠️ Tools Used

- **Languages:** Python, SQL  
- **Libraries:** `pyGAM`, `pandas`, `NumPy`, `Matplotlib`, `Seaborn`  
- **Visualization:** Tableau  
- **Techniques:** Spline Regression, Feature Engineering, Model Interpretation

---

## 💡 Key Takeaways

1. GAMs offer a perfect balance of flexibility and transparency for business modeling.
2. Understanding where depreciation changes slope can lead to smarter pricing strategies.
3. The best models are not just accurate—they’re explainable to the people who need them most.

---

**Contact:**  
[GitHub](https://github.com/brandyanalytics) | [LinkedIn](https://linkedin.com/in/brandyhorne01) | Brandyhorne01@gmail.com  
