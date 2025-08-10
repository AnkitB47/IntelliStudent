# Intelligent Student Score Prediction Platform

A compact end-to-end machine‑learning project that forecasts students’ math scores from demographic and academic attributes, complete with a web front end for real‑time predictions.

## 🚀 Overview
- **Automated pipeline:** Streamlines data ingestion, preprocessing, feature engineering, and hyper‑parameter tuning across **nine** regression algorithms.
- **Model leaderboard:** CatBoost cut RMSE by **67 %** (14.0 → 4.6) and reached **0.85 R²**, outperforming Random Forest (0.85 R²), AdaBoost (0.85 R²), XGBoost (0.83 R²), Lasso (0.83 R²), KNN (0.78 R²), and Decision Tree (0.75 R²), while Ridge and Linear Regression peaked at **0.88 R²**.
- **Flask deployment:** Delivers instant, personalized score predictions for educators via a simple web UI.

## 🗂 Project Structure
```
IntelliStudent/
│
├── application.py          # Flask entry point
├── src/                    # ML pipeline modules
│   ├── components/         # data_ingestion, transformation, model_training
│   ├── pipeline/           # predict & (placeholder) training pipelines
│   ├── utils.py            # common helpers (save/load objects, evaluation)
│   └── …
├── templates/              # HTML templates for Flask
├── notebook/               # data & exploratory notebooks
├── artifacts/              # generated models and preprocessors
└── requirements.txt        # Python dependencies
```

## 📦 Tech Stack
- **Python 3.x**, pandas, NumPy  
- **scikit‑learn**, XGBoost, CatBoost  
- **Flask** for deployment  
- HTML/CSS for the simple UI

## 📊 Dataset
Kaggle’s *Student Performance in Exams* dataset (`notebook/data/stud.csv`) containing gender, ethnicity, parental education, lunch type, test-preparation course, and reading/writing scores.

## 🔧 Setup & Installation
```bash
git clone <repository-url>
cd IntelliStudent
pip install -r requirements.txt
```

## 🏃️ Training the Model
```bash
python src/components/data_ingestion.py
```
This script performs data ingestion, transformation, model training, and stores the best model along with the preprocessing pipeline under `artifacts/`.

## 🌐 Running the Web App
```bash
python application.py
```
Open your browser at `http://localhost:5000` to input student details and receive predicted math scores.

## 📊 Results Snapshot
| Model                  | R²   | RMSE |
|------------------------|-----:|-----:|
| CatBoost               | 0.85 |  4.6 |
| Random Forest          | 0.85 |  5.0 |
| AdaBoost               | 0.85 |  5.1 |
| XGBoost                | 0.83 |  5.3 |
| Lasso                  | 0.83 |  5.4 |
| KNN                    | 0.78 |  6.0 |
| Decision Tree          | 0.75 |  6.3 |
| Ridge Regression       | 0.88 |  4.8 |
| Linear Regression      | 0.88 |  4.9 |

*(Metrics from cross‑validated experiments; RMSE in points.)*

## 🤝 Contributing
Pull requests are welcome—please open an issue to discuss your ideas before submitting major changes.

## 📜 License
This project is released under the MIT License.

---  
*Crafted to empower educators with data‑driven insights and lightning‑fast predictions.*
