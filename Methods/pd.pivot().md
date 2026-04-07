To reverse a melt, you use .pivot(). This takes those "long" rows and spreads them back out into "wide" columns.
## The Logic
Think of it as a 3-step instruction for Pandas:

   1. index: Which column stays as the row label?
   2. columns: Which column's unique values should become the new headers?
   3. values: Which column contains the actual data to fill the cells?

## Code Example: From Long back to Wide

import pandas as pd
# 1. Start with 'Long' data (the result of a melt)long_df = pd.DataFrame({
    'Name': ['Alice', 'Alice'],
    'Month': ['Jan', 'Feb'],
    'Sales': [10, 20]
})
# 2. Pivot it back to 'Wide'wide_df = long_df.pivot(index='Name', columns='Month', values='Sales')

print(wide_df)

Output:

| Name | Jan | Feb |
|---|---|---|
| Alice | 10 | 20 |

## Key Difference to Remember

* .melt(): Makes your data taller (more rows, fewer columns).
* .pivot(): Makes your data wider (fewer rows, more columns).

One thing to watch out for: if you have duplicate entries for the same index and column (e.g., two "Jan" sales for Alice), .pivot() will throw an error. In that case, you would use .pivot_table() instead to aggregate (average or sum) them.
SEE how to use .pivot_table() to handle those duplicate data cases?

