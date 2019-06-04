

* np.where
```
pd_df['col2'] = np.where(
     pd_df['col1'].between(0, 30, inclusive=False), 
    'option1', 
    'option2'
)

pd_df['difficulty'] = np.where(
     pd_df['Time'].between(0, 30, inclusive=False), 
    'Easy', 
     np.where(
        pd_df['Time'].between(0, 30, inclusive=False), 'Medium', 'Unknown'
     )
)
```

```
pd_df['difficulty'] = np.select(
    [
        pd_df['Time'].between(0, 30, inclusive=False), 
        pd_df['Time'].between(30, 60, inclusive=True)
    ], 
    [
        'Easy', 
        'Medium'
    ], 
    default='Unknown'
)

```

```
pd_df['difficulty'] = 'Unknown'
pd_df.loc[pd_df['Time'].between(0, 30, inclusive=False), 'difficulty'] = 'Easy'
pd_df.loc[pd_df['Time'].between(30, 60, inclusive=True), 'difficulty'] = 'Medium'
```

* np.stack : Stack the prescribed level(s) from columns to index
```
df.stack(level = 0, dropna=False)
```

* np.unstack()
```
df.stack()
```

* pivot
```df.pivot()```

* pivot_table
```df.pivot_table()```

* np.melt : Unpivots a DataFrame from wide format to long format
```
pd.melt(df, id_vars=['col1'], value_vars=['col2', 'col3'])
```
