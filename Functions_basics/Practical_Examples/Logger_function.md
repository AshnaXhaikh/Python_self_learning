### Example 2: Logger Function
```python
def log_message(level, *messages, **metadata):
    """Log messages with level and metadata"""
    print(f"[{level.upper()}]")
    for msg in messages:
        print(f"  {msg}")
    if metadata:
        print("  Metadata:", metadata)

log_message("info", "User logged in", "Session started", user_id=123, ip="192.168.1.1")
# Output:
# [INFO]
#   User logged in
#   Session started
#   Metadata: {'user_id': 123, 'ip': '192.168.1.1'}
```
