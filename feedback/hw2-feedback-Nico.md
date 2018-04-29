### ***Project 2 Feedback***

***Nico Van de Bovenkamp***

***

**Overall:**
Great work on this, Andrew! I hadn't ever bothered to do a `.groupby()` followed by `.describe()`! I usually just picked columns to work with and then perform some form of aggregation:

```python
admits.groupby(['prestige'])['gre'].agg(['min','max','mean','std'])
```
Everything looks good, but I think there are a couple of cases where you don't "catch" returned values. In other words, when you were trying to use the `admits.corr()` function, it "returned" the correlation matrix. However, you didn't catch the returned object in a new returned variable. You can do so as such:

```python
corr = admits.corr()
cmap = sns.diverging_palette(220, 10, as_cmap=True)
sns.heatmap(corr, cmap=cmap)
```

**Try that out!**
