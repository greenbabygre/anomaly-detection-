# Anomaly Detection

## What is anomaly detection?
Anomaly detection finds data points that differ greatly from the rest of the data, such as fraud, faults, or errors.

## Method: IQR (Interquartile Range)
1. Sort the data and find Q1 (25th percentile) and Q3 (75th percentile).
2. Compute IQR = Q3 - Q1.
3. Any value below Q1 - 1.5 x IQR or above Q3 + 1.5 x IQR is an anomaly.

IQR is not thrown off by extreme values. A Z-score approach can miss anomalies because extreme values inflate the standard deviation (the masking effect).

## How to run
```bash
python anomaly_detection.py
```

Example output:
```
Anomalies: [95, -40]
```

## Time complexity
- Time: O(n log n), because sorting is needed to find the quartiles
- Space: O(n)
