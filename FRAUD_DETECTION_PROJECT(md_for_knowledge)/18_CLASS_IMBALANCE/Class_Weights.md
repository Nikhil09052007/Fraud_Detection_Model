# Class Weights

Assigning a higher loss penalty to misclassifying the minority (fraud) class during training, without altering the actual data — an alternative to resampling.

## Key Points

- Often preferred over resampling since it doesn't discard or duplicate data
- Supported natively by most ML libraries via a `class_weight` or `scale_pos_weight` parameter
