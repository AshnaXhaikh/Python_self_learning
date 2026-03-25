```
### Order of Arguments

The correct order for mixing argument types is:

```python
def func(standard_args, *args, default_args="default", **kwargs):
    pass
```

**Rule:** `standard` → `*args` → `default` → `**kwargs`

---

## Argument Type Comparison

| Type | Syntax | Purpose | Example Call |
|------|--------|---------|--------------|
| Positional | `def f(a, b)` | Values in order | `f(1, 2)` |
| Keyword | `def f(a, b)` | Values by name | `f(b=2, a=1)` |
| Default | `def f(a=1, b=2)` | Provide defaults | `f()` |
| `*args` | `def f(*args)` | Variable positional | `f(1, 2, 3)` |
| `**kwargs` | `def f(**kwargs)` | Variable keyword | `f(a=1, b=2)` |

---

```
