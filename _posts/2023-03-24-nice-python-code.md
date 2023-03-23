---
author: isaac
title: Code for looping a bunch of schema versions
---

My first code explanation! I feel that it is very helpful to share innovative approches to solving problems to the world, as long it doesn't contain any PII!
Code is beautiful in itself. However, any innovative code cannot be known to the world if we don't document it/ explain it thoroughly.

From a securities perspective, understandibility of code helps all people understand what is going on in their systems. And that means they can be harder to exploit/ attack.

```python
import pandas as pd
# use a dataframe to concatenate
numbers = list(range(1,100))
# this creates a list of numbers from 1 - 99
svs = ['sv' + str(num) for num in numbers]
# this savvy looking tool is concatenating the literal string sv, for schema version to all the strings
# a.k.a. the list comprehension :)
print(svs)
# print these just to check we have all 99
df_concatenated = pd.DataFrame()
# this code is used to declare a DataFrame object from the pandas library
for sv in svs:
    qs = f'''SELECT MIN(load_dt), MAX(load_dt)
    FROM schema_1.curated_{svs}'''
    df = aws.execute_query_df(db, qs)
    df_concatenated = pd.concat([df_concatenated, df], axis = 0)
# this loop goes through the list of schema versions and executes the above query qs
# then we use the concat function. Axis = 0 just means you are performing a computation accross all rows
print(df_concatenated)
# make sure the print command is outside the loop
```
