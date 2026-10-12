# Module 2 — House Prices: предобработка и регрессия

**Автор:** Корнеева Елизавета, АСОиУб-23-2   
**Дата:** 2026-10-12  

---

## Результаты

| Модель | RMSE (log) | MAE (log) | R² | RMSE ($) |
|--------|-----------|-----------|-----|----------|
| Linear Regression | 0.135 | 0.095 | 0.88 | $28 000 |
| Ridge | 0.128 | 0.090 | 0.90 | $26 000 |
| **Lasso** | **0.125** | **0.088** | **0.91** | **$25 000** |
| ElasticNet | 0.126 | 0.089 | 0.91 | $25 500 |

**Лучшая модель:** Lasso (R² = 0.91).  
**Время обучения:** < 0.5 сек на каждую модель.

---

## Быстрый старт

```bash
git clone https://github.com/KorneevaElizaveta/ml-course-korneeva.git
cd ml-course-Korneeva/module-2-house-prices
pip install -r requirements.txt
jupyter notebook notebook.ipynb
