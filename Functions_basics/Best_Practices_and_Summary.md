---

## Best Practices

1. **Use nested functions** when helper logic is only relevant inside the outer function
2. **Avoid deep nesting** (more than 2-3 levels) as it reduces readability
3. **Use `nonlocal` sparingly**; consider classes if you need complex state
4. **Document nested functions** clearly, especially when returned as closures

---

## Summary

| Concept | Description |
|---------|-------------|
| **Nested Function** | Function defined inside another function |
| **Closure** | Inner function that remembers outer scope |
| **nonlocal** | Keyword to modify outer (non-global) variables |
| **Encapsulation** | Hiding helper functions from global scope |

```
