# Model Performance Monitoring

Continuously tracking live model metrics (precision, recall, score distributions) against expectations, using delayed-but-eventually-available true labels.

## Key Points

- Complicated by label delay (Section 08) — true performance often can't be measured until weeks after prediction
- Proxy metrics (e.g. score distribution shifts) can provide earlier warning signs before true labels arrive
