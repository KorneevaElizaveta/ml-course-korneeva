# Module 1 — Titanic: EDA + бинарная классификация

**Автор:** Корнеева Елизавета  
**Группа:** АСОиУб-23-2   
**Дата:** 2026-09-29  
**Дисциплина:** Машинное обучение и ИИ    

---

## 📊 Результаты

| Модель | Accuracy | Precision | Recall | F1 | ROC-AUC | Время обучения |
|--------|----------|-----------|--------|-----|---------|----------------|
| Logistic Regression | 0.83 | 0.81 | 0.76 | 0.78 | **0.86** | ~0.01 сек |
| Decision Tree | 0.79 | 0.75 | 0.71 | 0.73 | 0.81 | ~0.005 сек |

**Лучшая модель:** Logistic Regression (ROC-AUC = 0.86).


---

## Обработка данных

- `Age` (20% пропусков) — заполнен медианой по группам `Pclass + Sex`.
- `Embarked` (0.2% пропусков) — заполнен модой.
- `Cabin` (77% пропусков) — удалён.
- **Feature Engineering:**
  - `Family_Size = SibSp + Parch + 1`
  - `Is_Alone = (Family_Size == 1)`
  - `Age_Group` — биннинг через `pd.cut()`
- **Кодирование:**
  - `Sex` → Label Encoding
  - `Embarked`, `Age_Group` → One-Hot Encoding

---

##  Быстрый старт

### Установка зависимостей

```bash
import joblib
import requests
from io import BytesIO

BASE_URL = "https://raw.githubusercontent.com/KorneevaElizaveta/ml-course-korneeva/main/module-1-titanic"
model = joblib.load(BytesIO(requests.get(f"{BASE_URL}/models/lr_model.pkl").content))