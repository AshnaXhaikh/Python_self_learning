---

## Practical Examples

### Example 1: Custom Sorting with Multiple Keys
```python
students = [
    {'name': 'Alice', 'grade': 85, 'age': 20},
    {'name': 'Bob', 'grade': 92, 'age': 19},
    {'name': 'Charlie', 'grade': 85, 'age': 22},
]

# Sort by grade descending, then by age ascending
sorted_students = sorted(students, key=lambda x: (-x['grade'], x['age']))
print(sorted_students)
```

### Example 2: Data Transformation
```python
# Format names to title case
names = ["john doe", "jane smith", "bob johnson"]
formatted = list(map(lambda x: x.title(), names))
print(formatted)  # Output: ['John Doe', 'Jane Smith', 'Bob Johnson']

# Extract initials
initials = list(map(lambda x: ''.join(word[0].upper() for word in x.split()), names))
print(initials)  # Output: ['JD', 'JS', 'BJ']
```

### Example 3: Conditional Filtering
```python
# Filter and transform in one step
numbers = [-5, -2, 0, 3, 7, -1, 4]

# Get positive squares
positive_squares = list(map(lambda x: x**2, filter(lambda x: x > 0, numbers)))
print(positive_squares)  # Output: [9, 49, 16]
```

