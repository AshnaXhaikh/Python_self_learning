---

## Practical Examples

### Example 1: Data Validation with Factory
```python
def create_validator(min_value, max_value):
    """Create a custom range validator"""
    
    def validator(value):
        if not (min_value <= value <= max_value):
            raise ValueError(f"{value} must be between {min_value} and {max_value}")
        return True
    
    return validator

# Create validators
age_validator = create_validator(0, 120)
score_validator = create_validator(0, 100)

age_validator(25)   # ✅ Pass
# age_validator(150)  # ❌ Raises ValueError
score_validator(85)  # ✅ Pass
```

