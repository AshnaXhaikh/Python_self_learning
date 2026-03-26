```markdown
graph TD
    A[Need a placeholder?] --> B{Where?}
    
    B --> C[Function/Method]
    B --> D[Class]
    B --> E[Conditional]
    B --> F[Loop]
    B --> G[Exception]
    
    C --> H{Will it be implemented?}
    H -->|Yes| I[Use pass]
    H -->|No| J[Use return None]
    H -->|Abstract| K[Use raise NotImplementedError]
    
    D --> L[Use pass for empty class]
    
    E --> M[Use pass to skip branch]
    
    F --> N[Use pass to skip iteration]
    
    G --> O[Use pass to ignore error]
```
