# 16 — Data Leakage and Time

One of the most common and most damaging mistakes in fraud modeling: accidentally letting future information leak into training features, producing models that look great offline but fail in production. This folder is dedicated entirely to avoiding that trap.

## Key Points

- Read this folder carefully even if you've done feature engineering before — fraud data is especially leakage-prone
- A model with leakage can show excellent offline metrics and still fail completely live
