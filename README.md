markdown
Copy
# Simple Sampling

This code demonstrates how to perform simple random sampling using Python. The method involves choosing elements with equal probability of being chosen.

## Steps:

1. **Import the necessary libraries:**
   ```python
   import numpy as np
   import pandas as pd
Read the CSV file:
   ```python
   data = pd.read_csv('your_file.csv')
   ```
2. **Verify its size:**
```python
print(data.shape)
```
3. **Use np.random.seed to reproduce the experiment:**
```python
np.random.seed(42)  # For reproducible results
```
4. **Create a sample using np.random.choice:**
```python
sample = np.random.choice(
    [0, 1],              # Variables to choose from
    size=150,            # Sample size
    replace=True,        # With replacement
    p=[0.7, 0.3]        # Probabilities for each variable
)
```
5. **Analyze the results:**
```python
print("Number of 0s:", sum(sample == 0))  # ~70% of elements (expected ~105)
print("Number of 1s:", sum(sample == 1))  # ~30% of elements (expected ~45)
```
