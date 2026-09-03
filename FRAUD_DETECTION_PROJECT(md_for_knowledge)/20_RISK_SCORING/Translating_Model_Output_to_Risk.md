# Translating Model Output to Risk

The end-to-end process: raw model probability → calibration → combination with impact/amount → risk score → risk band, ready for the decision engine to act on.

## Key Points

- Each step should be validated independently — a miscalibrated score corrupts every downstream decision
- This pipeline is where data science output becomes an operational business tool
