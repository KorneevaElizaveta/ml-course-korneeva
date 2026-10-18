# Module 3 — Customer Churn: Ансамблевые методы

**Автор:** Корнеева Елизавета, АСОиУб-23-2  
**Дата:** 2026-18-10   
**Датасет:** Telco Customer Churn

---

## 🎯 Цель работы

Освоить ансамблевые методы машинного обучения (Bagging и Boosting) на примере задачи прогнозирования оттока клиентов, провести оптимизацию гиперпараметров через Optuna и интерпретировать модель с помощью SHAP.

---

## 📊 Результаты моделей

| Модель | Accuracy | Precision | Recall | F1 | ROC-AUC |
|--------|----------|-----------|--------|-----|---------|
| Random Forest | 0.78 | 0.65 | 0.72 | 0.68 | 0.83 |
| XGBoost | 0.79 | 0.67 | 0.73 | 0.70 | 0.84 |
| LightGBM | 0.80 | 0.68 | 0.74 | 0.71 | 0.84 |
| CatBoost | 0.79 | 0.66 | 0.75 | 0.70 | 0.84 |
| **LightGBM (Optuna)** | **0.81** | **0.70** | **0.76** | **0.73** | **0.85+** |

**Лучшая модель:** LightGBM после оптимизации гиперпараметров через Optuna.


---

## 📁 Структура модуля

```text
module-3-churn/
├── README.md               
├── notebook.ipynb          
├── requirements.txt        
├── data/
│   ├── telco_churn.csv     
│   └── churn_info.md       
├── models/
│   ├── best_model.pkl      
│   ├── rf_model.pkl        
│   ├── xgb_model.pkl       
│   ├── lgbm_model.pkl      
│   ├── cat_model.pkl       
│   ├── feature_cols.json   
│   └── metrics.json        
└── examples/
    ├── eda_plots.png       
    ├── roc_curves.png      
    ├── feature_importance.png
    ├── shap_summary.png    
    └── shap_waterfall.png  