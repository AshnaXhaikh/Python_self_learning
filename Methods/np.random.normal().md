## 📝 Python Data Simulation Cheatsheet
This README covers the logic for generating, joining, and cleaning synthetic datasets using NumPy.
------------------------------
## 1. np.random.normal(loc, scale, size)
Purpose: Generates "fake" data that follows a Bell Curve (Normal Distribution).

* loc (Mean): The center of the curve (the average value).
* scale (Standard Deviation): The "spread" of the data.
* Tip: ~68% of your data will fall within mean ± 1 SD.
   * Warning: If the SD is large relative to the Mean, you may get negative numbers.
* size: How many data points to create.

Example:

# Average bill $22, spread of $9, 90 customersdinner = np.random.normal(22, 9, 90) 

```
1. Why you see negative values
Even though your mean is 
 and standard deviation (SD) is 
, the "13 to 31" range only covers about 68% of the data (the 68-95-99.7 rule).
Mean - 1 SD: 


Mean - 2 SD: 


Mean - 3 SD: 



Since you generated 90 points, there is a statistical chance that a few points will fall more than 2 SDs away from the mean, dropping below zero.
```
