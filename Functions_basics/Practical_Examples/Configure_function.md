## Practical Examples

### Example 1: Configuration Function
```python
def configure_app(**kwargs):
    """Configure application with flexible settings"""
    settings = {
        'debug': False,
        'host': 'localhost',
        'port': 8080
    }
    settings.update(kwargs)
    return settings

config = configure_app(debug=True, port=3000)
print(config)  # {'debug': True, 'host': 'localhost', 'port': 3000}
```

