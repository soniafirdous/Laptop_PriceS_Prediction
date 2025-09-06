# 💻 Laptop Price Prediction

This project aims to predict laptop prices based on their specifications using regression models. 

The dataset includes detailed features such as company, processor, memory, GPU, operating system, and display characteristics.

A logarithmic transformation was applied to the target variable (price) to handle skewness and reduce the impact of extreme values.

📌 Dataset Description

Key features in the dataset:

Company → Laptop manufacturer

TypeName → Laptop type (Ultrabook, Notebook, Gaming, etc.)

Inches → Screen size in inches

ScreenResolution → Display resolution

Cpu → Full CPU name

Ram → System memory (GB)

Memory → Storage information (HDD/SSD)

Gpu → Graphics card

OpSys → Operating system

Weight → Laptop weight (kg)

Touchscreen → Whether the laptop has a touchscreen (0/1)

IPS → IPS display indicator (0/1)

PPI → Pixels per inch (calculated from resolution and screen size)

Cpu_brand → Extracted CPU brand (Intel, AMD, etc.)

HDD / SSD → Separated storage features

Gpu brand → Extracted GPU brand

OS → Simplified operating system category

Price (target) → Laptop price (log-transformed for modeling)

🎯 Objective

Predict laptop prices based on specifications.

Compare Linear Regression, Ridge, and Lasso models after applying log transformation.

Evaluate using R², MAE, and RMSE.

📊 Model Performance (Test Set)

Model	R²	MAE	RMSE

Linear Regression	0.813	0.209	—

Lasso Regression (α=0.001)	0.807	0.211	0.272

Ridge Regression (Best α)	0.807	0.210	0.271

Linear Regression performed best with R² = 0.813 and lowest MAE.

Ridge and Lasso gave nearly identical results (R² ≈ 0.807).

MAE ≈ 0.21 (log scale) → Back-transformed (exp(0.21) ≈ 1.23), predictions are on average about 23% higher or lower than actual laptop prices.

🔎 Interpretation

Log transformation improved error stability and reduced the effect of very expensive laptops.

Regularization (Ridge, Lasso) did not significantly improve results, indicating no severe multicollinearity.

Lasso is still useful for feature selection and interpretability.

Key predictive features: Company, RAM, CPU brand, GPU brand, storage (SSD/HDD), and display quality (PPI, touchscreen, IPS).

🚀 Next Steps

Explore feature interactions (e.g., RAM × GPU, CPU × SSD).

Experiment with non-linear models (Random Forest, Gradient Boosting, XGBoost) for better accuracy.

👩‍💻 Author

Project by Sonia Firdous. 

Special thanks to my teacher Aqsa Moiz for guidance 🙏
