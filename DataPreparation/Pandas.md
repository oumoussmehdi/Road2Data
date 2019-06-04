

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

* np.melt
```

```
