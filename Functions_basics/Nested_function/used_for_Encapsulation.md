
---

## Why Use Nested Functions?

### 1. **Encapsulation**
Hide helper functions that shouldn't be accessible globally.

```python
def calculate_average(numbers):
    """Calculate average with helper function hidden"""
    
    def validate_data(data):
        """Helper function (not accessible outside)"""
        if not data:
            raise ValueError("Empty list")
        return True
    
    validate_data(numbers)
    return sum(numbers) / len(numbers)

# validate_data() is NOT accessible here
# Only calculate_average() is exposed
```
