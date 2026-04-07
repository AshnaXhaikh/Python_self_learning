## 3. np.clip(array, a_min, a_max)
Purpose: Keeps values within a specific "safety" range. It "trims" outliers to your boundaries.

* a_min: The floor. Anything lower than this becomes this value.
* a_max: The ceiling. Anything higher than this becomes this value.
* None: Use this if you don't want a limit on one side.

Example:

# Remove negative bills: # If value < 0, make it 0. If value > 0, leave it alone.clean_dinner = np.clip(dinner, 0, None)

| Function | Goal | Real-World Analogy |
|---|---|---|
| .clip() | Clean Data | Setting a "speed limit" (min/max). |
